---
UID: NS:vdssys._MIRROR_VIRTUAL_DISK_PARAMETERS
title: "_MIRROR_VIRTUAL_DISK_PARAMETERS"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) mirror request parameters.
old-location: vhd\mirror_virtual_disk_parameters.htm
old-project: VStor
ms.assetid: bcde890e-24d5-41ac-8e5a-ba0d99e395e1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PMIRROR_VIRTUAL_DISK_PARAMETERS, MIRROR_VIRTUAL_DISK_PARAMETERS, MIRROR_VIRTUAL_DISK_PARAMETERS structure [VHD], PMIRROR_VIRTUAL_DISK_PARAMETERS, PMIRROR_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _MIRROR_VIRTUAL_DISK_PARAMETERS, vdssys/MIRROR_VIRTUAL_DISK_PARAMETERS, vdssys/PMIRROR_VIRTUAL_DISK_PARAMETERS, vhd.mirror_virtual_disk_parameters, virtdisk/MIRROR_VIRTUAL_DISK_PARAMETERS, virtdisk/PMIRROR_VIRTUAL_DISK_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdssys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MIRROR_VIRTUAL_DISK_PARAMETERS, *PMIRROR_VIRTUAL_DISK_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - MIRROR_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

