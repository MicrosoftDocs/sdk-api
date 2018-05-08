---
UID: TP:sr
ms.assetid: 40d297e6-ff66-3421-9344-6dcb60c30222
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# System Restore



Overview of the System Restore technology.

To develop System Restore, you need these headers:

 * [srrestoreptapi.h](..\srrestoreptapi\index.md)

For the programming guide, see [System Restore](https://review.docs.microsoft.com/en-us/win32-test/sr).

## Functions

| Title   | Description   |
| ---- |:---- |
| [SRRemoveRestorePoint function](..\srrestoreptapi\nf-srrestoreptapi-srremoverestorepoint.md) | Deletes the specified restore point. |
| [SRSetRestorePointA function](..\srrestoreptapi\nf-srrestoreptapi-srsetrestorepointa.md) | Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point. |
| [SRSetRestorePointW function](..\srrestoreptapi\nf-srrestoreptapi-srsetrestorepointw.md) | Specifies the beginning and the ending of a set of changes so that System Restore can create a restore point. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [_RESTOREPTINFOA structure](..\srrestoreptapi\ns-srrestoreptapi-_restoreptinfoa.md) | Contains information used by the SRSetRestorePoint function. |
| [_RESTOREPTINFOW structure](..\srrestoreptapi\ns-srrestoreptapi-_restoreptinfow.md) | Contains information used by the SRSetRestorePoint function. |
| [_SMGRSTATUS structure](..\srrestoreptapi\ns-srrestoreptapi-_smgrstatus.md) | Contains status information used by the SRSetRestorePoint function. |
