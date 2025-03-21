=====================
``mc license update``
=====================

.. default-domain:: minio

.. contents:: Table of Contents
   :local:
   :depth: 1

.. mc:: mc license update

Description
-----------

.. start-mc-license-update-desc

Use the :mc-cmd:`mc license update` command to replace a license key for a deployment.

.. end-mc-license-update-desc

For deployments registered for |SUBNET|, MinIO automatically checks for and updates the license every month.

Examples
--------

Update the License Key for a Deployment with Alias ``minio1``
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell
   :class: copyable

   mc license update minio1 license.key

Syntax
------
      
The command has the following syntax:

.. code-block:: shell

   mc [GLOBALFLAGS] license update                   \
                            ALIAS                    \
                            [LICENSE-FILE-WITH-PATH] \
                            [--airgap]

Parameters
~~~~~~~~~~

.. mc-cmd:: ALIAS
   :required:

   The :ref:`alias <alias>` of the MinIO deployment.

.. mc-cmd:: LICENSE-FILE-WITH-PATH
   :optional:

   The path (relative to the current working directory) and file name of the key to use to update the deployment's license.

   To download the API key from SUBNET:

   #. Log in to |SUBNET|
   #. Go to the :guilabel:`Deployments` tab
   #. Select the :guilabel:`API Key` button near the top of the page on the right side of the account statistics information box
   #. Select copy button to the right of the key field to copy the key value to your clipboard

   
.. mc-cmd:: --airgap
   :optional:

   Use in environments without network access to SUBNET (for example, airgapped, firewalled, or similar configuration).

   If the deployment is airgapped, but the local device where you are using the :ref:`minio client <minio-client>` has network access, you do not need to use the ``--airgap`` flag.

Global Flags
~~~~~~~~~~~~

.. include:: /includes/common-minio-mc.rst
   :start-after: start-minio-mc-globals
   :end-before: end-minio-mc-globals
