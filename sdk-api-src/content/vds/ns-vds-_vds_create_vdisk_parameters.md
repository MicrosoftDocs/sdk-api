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

# _VDS_CREATE_VDISK_PARAMETERS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Contains the parameters to be used when a virtual disk is created.


## -struct-fields




### -field UniqueId

A unique GUID value to be assigned to the virtual disk.


### -field MaximumSize

The maximum virtual size, in bytes, of the virtual disk object.


### -field BlockSizeInBytes

The internal block size, in bytes, of the virtual disk object.


### -field SectorSizeInBytes

Internal sector size, in bytes, of the virtual disk object.


### -field pParentPath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a parent virtual disk object. This member associates the new virtual disk with an existing virtual disk.


### -field pSourcePath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a source of data to be copied to the new virtual disk.


## -see-also




<a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">IVdsVdProvider::CreateVDisk</a>
 

 

