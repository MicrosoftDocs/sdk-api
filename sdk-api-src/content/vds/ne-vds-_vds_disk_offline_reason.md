---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VDS_DISK_OFFLINE_REASON enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of reasons for a disk to be offline.


## -enum-fields




### -field VDSDiskOfflineReasonNone

The reason is unknown.


### -field VDSDiskOfflineReasonPolicy

The disk is offline because of the current <a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">SAN policy</a>.


### -field VDSDiskOfflineReasonRedundantPath

The disk is offline because it has a path that is the same as that of another device. This value is used when multipathing is physically enabled, but the MPIO software is not installed or is not functioning properly. (When the MPIO software is functioning properly, it exposes only one disk device.)


### -field VDSDiskOfflineReasonSnapshot

The disk is offline because it contains a volume shadow copy volume. In this case, the disk is a clone of another disk that is online.


### -field VDSDiskOfflineReasonCollision

If the disk is an MBR disk, it is offline because its disk signature is the same as that of another disk that is online. The disk signature is found in the <b>dwSignature</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structures and in the <b>Signature</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552668">DRIVE_LAYOUT_INFORMATION_MBR</a> structure.

If it is a GPT disk, it is offline for one of the following reasons:<ul>
<li>Its disk identifier is the same as that of another disk that is offline. The disk identifier is found in the <b>DiskGuid</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> and <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structures and in the <b>DiskId</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552664">DRIVE_LAYOUT_INFORMATION_GPT</a> structure.</li>
<li>One of the partitions has the same partition GUID as another partition on the same disk.</li>
</ul>



### -field VDSDiskOfflineReasonResourceExhaustion


### -field VDSDiskOfflineReasonWriteFailure


### -field VDSDiskOfflineReasonDIScan


### -field VDSDiskOfflineReasonLostDataPersistence




## -see-also




<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>
 

 

