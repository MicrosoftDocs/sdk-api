---
UID: TP:dedup
ms.assetid: cd834ca0-b712-386c-8042-173e3d8c8820
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Data Deduplication API



Overview of the Data Deduplication API technology.

To develop Data Deduplication API, you need these headers:

 * [ddpbackup.h](..\ddpbackup\index.md)

For the programming guide, see [Data Deduplication API](/previous-versions/windows/desktop/dedup).

## Structures

| Title   | Description   |
| ---- |:---- |
| [_DDP_FILE_EXTENT structure](..\ddpbackup\ns-ddpbackup-_ddp_file_extent.md) | DDP_FILE_EXTENT represents the extent of data in a file that is to be read in a pending call to ReadBackupFile. |
| [_DEDUP_CONTAINER_EXTENT structure](..\ddpbackup\ns-ddpbackup-_dedup_container_extent.md) | A logical container file may be stored in a single segment or multiple segments in the backup store. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration](..\ddpbackup\ne-ddpbackup-_dedup_backup_support_param_type.md) | Indicates whether Data Deduplication should perform an unoptimized or optimized restore. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDedupBackupSupport interface](..\ddpbackup\nn-ddpbackup-idedupbackupsupport.md) | Provides a method for restoring a file from a backup store containing copies of Data Deduplication reparse points, metadata, and container files. |
| [IDedupReadFileCallback interface](..\ddpbackup\nn-ddpbackup-idedupreadfilecallback.md) | A callback interface, implemented by backup applications, that enables Data Deduplication to read content from metadata and container files residing in a backup store and optionally improve restore efficiency. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDedupBackupSupport::RestoreFiles](..\ddpbackup\nf-ddpbackup-idedupbackupsupport-restorefiles.md) | Reconstructs a set of files from a backup store that contains the fully optimized version of the files (reparse points) and the Data Deduplication store. |
| [IDedupReadFileCallback::OrderContainersRestore](..\ddpbackup\nf-ddpbackup-idedupreadfilecallback-ordercontainersrestore.md) | This method provides the application with the ability to influence the order of the pending reads that are required to retrieve the target file. |
| [IDedupReadFileCallback::PreviewContainerRead](..\ddpbackup\nf-ddpbackup-idedupreadfilecallback-previewcontainerread.md) | Provides the application with a preview of the sequence of reads that are pending for a given container file extent. |
| [IDedupReadFileCallback::ReadBackupFile](..\ddpbackup\nf-ddpbackup-idedupreadfilecallback-readbackupfile.md) | Reads data from a Data Deduplication store metadata or container file located in the backup store. |
