---
UID: TP:wsb
ms.assetid: d329838b-7159-34cd-b2ce-9c345c166b33
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Windows Server Backup



Overview of the Windows Server Backup technology.

To develop Windows Server Backup, you need these headers:

 * [wsbapp.h](..\wsbapp\index.md)
 * [wsbonline.h](..\wsbonline\index.md)

For the programming guide, see [Windows Server Backup](/previous-versions/windows/desktop/wsb).

## Functions

| Title   | Description   |
| ---- |:---- |
| [DeregisterOnlineBackupFromWindowsServerBackup function](..\wsbonline\nf-wsbonline-deregisteronlinebackupfromwindowsserverbackup.md) | De-registers an already registered Cloud backup provider. |
| [RegisterOnlineBackupWithWindowsServerBackup function](..\wsbonline\nf-wsbonline-registeronlinebackupwithwindowsserverbackup.md) | Registers a Cloud backup provider with Windows Server Backup. |
| [UpdateOBStatusInWindowsServerBackup function](..\wsbonline\nf-wsbonline-updateobstatusinwindowsserverbackup.md) | Updates the Cloud backup provider status in the Windows Server Backup MMC snap-in. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_WSB_OB_REGISTRATION_INFO structure](..\wsbonline\ns-wsbonline-_wsb_ob_registration_info.md) | Contains information to register a cloud backup provider with Windows Server Backup. |
| [_WSB_OB_STATUS_ENTRY structure](..\wsbonline\ns-wsbonline-_wsb_ob_status_entry.md) | Contains status information for one entry to be shown in the Windows Server Backup MMC snap-in. |
| [_WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR structure](..\wsbonline\ns-wsbonline-_wsb_ob_status_entry_value_type_pair.md) | Contains the value and value type for a parameter used to expand the value resource string. |
| [_WSB_OB_STATUS_INFO structure](..\wsbonline\ns-wsbonline-_wsb_ob_status_info.md) | Contains information to update the cloud backup provider status in the Windows Server Backup MMC snap-in. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [_WSB_OB_STATUS_ENTRY_PAIR_TYPE enumeration](..\wsbonline\ne-wsbonline-_wsb_ob_status_entry_pair_type.md) | Indicates the type of the parameter value. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IWsbApplicationAsync interface](..\wsbapp\nn-wsbapp-iwsbapplicationasync.md) | Defines methods to monitor and control the progress of an asynchronous operation. |
| [IWsbApplicationBackupSupport interface](..\wsbapp\nn-wsbapp-iwsbapplicationbackupsupport.md) | Defines a method for checking the consistency of the application's VSS writer's components. |
| [IWsbApplicationRestoreSupport interface](..\wsbapp\nn-wsbapp-iwsbapplicationrestoresupport.md) | Defines methods for performing application-specific restore tasks. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IWsbApplicationAsync::Abort](..\wsbapp\nf-wsbapp-iwsbapplicationasync-abort.md) | Cancels an incomplete asynchronous operation. |
| [IWsbApplicationAsync::QueryStatus](..\wsbapp\nf-wsbapp-iwsbapplicationasync-querystatus.md) | Queries the status of an asynchronous operation. |
| [IWsbApplicationBackupSupport::CheckConsistency](..\wsbapp\nf-wsbapp-iwsbapplicationbackupsupport-checkconsistency.md) | Checks the consistency of the VSS writer's components in the shadow copy after shadow copies are created for the volumes to be backed up. |
| [IWsbApplicationRestoreSupport::IsRollForwardSupported](..\wsbapp\nf-wsbapp-iwsbapplicationrestoresupport-isrollforwardsupported.md) | Reports whether the application supports roll-forward restore. |
| [IWsbApplicationRestoreSupport::OrderComponents](..\wsbapp\nf-wsbapp-iwsbapplicationrestoresupport-ordercomponents.md) | Specifies the order in which application components are to be restored. |
| [IWsbApplicationRestoreSupport::PostRestore](..\wsbapp\nf-wsbapp-iwsbapplicationrestoresupport-postrestore.md) | Performs application-specific PostRestore operations. |
| [IWsbApplicationRestoreSupport::PreRestore](..\wsbapp\nf-wsbapp-iwsbapplicationrestoresupport-prerestore.md) | Performs application-specific PreRestore operations. |
