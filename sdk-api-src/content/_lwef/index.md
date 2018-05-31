---
UID: TP:lwef
ms.assetid: 384117d0-d2cd-3434-b330-5f546ef90ab4
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Legacy Windows Environment Features



Overview of the Legacy Windows Environment Features technology.

To develop Legacy Windows Environment Features, you need these headers:

 * [emptyvc.h](..\emptyvc\index.md)
 * [mmcobj.h](..\mmcobj\index.md)
 * [provider.h](..\provider\index.md)
 * [searchapi.h](..\searchapi\index.md)
 * [shldisp.h](..\shldisp\index.md)
 * [shlobj_core.h](..\shlobj_core\index.md)
 * [windowsdefender.h](..\windowsdefender\index.md)
 * [wmiutils.h](..\wmiutils\index.md)

For the programming guide, see [Legacy Windows Environment Features](/windows/desktop/lwef).

## Functions

| Title   | Description   |
| ---- |:---- |
| [WDEnable function](..\windowsdefender\nf-windowsdefender-wdenable.md) | Changes Windows Defender status to on or off. |
| [WDStatus function](..\windowsdefender\nf-windowsdefender-wdstatus.md) | Returns the current status of Windows Defender. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [ColumnSortOrder enumeration](..\mmcobj\ne-mmcobj-columnsortorder.md) | Used by IResultsViewer |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IEmptyVolumeCache interface](..\emptyvc\nn-emptyvc-iemptyvolumecache.md) | Used by the disk cleanup manager to communicate with a disk cleanup handler. Exposes methods that enable the manager to request information from a handler, and notify it of events such as the start of a scan or purge. |
| [IEmptyVolumeCache2 interface](..\emptyvc\nn-emptyvc-iemptyvolumecache2.md) | Extends IEmptyVolumeCache. This interface defines one additional method, InitializeEx, that provides better localization support than IEmptyVolumeCache |
| [IEmptyVolumeCacheCallBack interface](..\emptyvc\nn-emptyvc-iemptyvolumecachecallback.md) | Exposes methods that are used by a disk cleanup handler to communicate with the disk cleanup manager. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IEmptyVolumeCache2::InitializeEx](..\emptyvc\nf-emptyvc-iemptyvolumecache2-initializeex.md) | Initializes the disk cleanup handler. It provides better support for localization than Initialize. |
| [IEmptyVolumeCache::Deactivate](..\emptyvc\nf-emptyvc-iemptyvolumecache-deactivate.md) | Notifies the handler that the disk cleanup manager is shutting down. |
| [IEmptyVolumeCache::GetSpaceUsed](..\emptyvc\nf-emptyvc-iemptyvolumecache-getspaceused.md) | Requests the amount of disk space that the disk cleanup handler can free. |
| [IEmptyVolumeCache::Initialize](..\emptyvc\nf-emptyvc-iemptyvolumecache-initialize.md) | Initializes the disk cleanup handler, based on the information stored under the specified registry key. |
| [IEmptyVolumeCache::Purge](..\emptyvc\nf-emptyvc-iemptyvolumecache-purge.md) | Notifies the handler to start deleting its unneeded files. |
| [IEmptyVolumeCache::ShowProperties](..\emptyvc\nf-emptyvc-iemptyvolumecache-showproperties.md) | Notifies the handler to display its UI. |
| [IEmptyVolumeCacheCallBack::PurgeProgress](..\emptyvc\nf-emptyvc-iemptyvolumecachecallback-purgeprogress.md) | Called periodically by a disk cleanup handler to update the disk cleanup manager on the progress of a purge of deletable files. |
| [IEmptyVolumeCacheCallBack::ScanProgress](..\emptyvc\nf-emptyvc-iemptyvolumecachecallback-scanprogress.md) | Called by a disk cleanup handler to update the disk cleanup manager on the progress of a scan for deletable files. |
