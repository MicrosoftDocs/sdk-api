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

# _MIRROR_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD) mirror request parameters.


## -struct-fields




### -field Version

Indicates the version of this structure to use. Set this to 
      <b>MIRROR_VIRTUAL_DISK_VERSION_1</b> (1).


### -field Version1

This structure is used if the <b>Version</b> member is set to 
       <b>MIRROR_VIRTUAL_DISK_VERSION_1</b>.


### -field Version1.MirrorVirtualDiskPath


<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Fully qualified</a> path where the mirrored 
         virtual disk will be located. If the <i>Flags</i> parameter to 
         <a href="https://msdn.microsoft.com/eb72043a-7515-42c0-900d-feed4503ea7a">MirrorVirtualDisk</a> is 
         <b>MIRROR_VIRTUAL_DISK_FLAG_NONE</b> (0) then this file must not exist. If the 
         <i>Flags</i> parameter to 
         <b>MirrorVirtualDisk</b> is 
         <b>MIRROR_VIRTUAL_DISK_FLAG_EXISTING_FILE</b> (1) then this file must exist.


## -see-also




<a href="https://msdn.microsoft.com/eb72043a-7515-42c0-900d-feed4503ea7a">MirrorVirtualDisk</a>



<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

