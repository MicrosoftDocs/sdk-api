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

# _VDS_VDISK_PROPERTIES structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a virtual disk.


## -struct-fields




### -field Id

Unique VDS-specific session identifier of the disk.


### -field State

A <a href="https://msdn.microsoft.com/62906f28-f6ae-488c-bf1f-655de5c7b95e">VDS_VDISK_STATE</a> enumeration value that specifies the virtual disk state.


### -field VirtualDeviceType

A pointer to a <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure that specifies the storage device type of the virtual disk.


### -field VirtualSize

The size, in bytes, of the virtual disk.


### -field PhysicalSize

The on-disk size, in bytes, of the virtual disk backing file.


### -field pPath

A <b>NULL</b>-terminated wide-character string containing the name and directory path of the backing file for the virtual disk.




### -field pDeviceName

A <b>NULL</b>-terminated wide-character string containing the name and device path of the disk device object for the volume where the virtual disk resides.


### -field DiskFlag

A bitmask of <a href="https://msdn.microsoft.com/f22bcf17-59fd-4a05-9516-2e14f173ed33">DEPENDENT_DISK_FLAG</a> enumeration values that specify disk dependency information.


### -field bIsChild

<b>TRUE</b> if the virtual disk is a child virtual disk, or <b>FALSE</b> otherwise.


### -field pParentPath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a parent virtual disk object.


## -see-also




<a href="https://msdn.microsoft.com/0ecfbd1f-2f67-4d79-b081-7df071b070a4">IVdsVDisk::GetProperties</a>
 

 

