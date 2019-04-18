---
UID: NS:virtdisk._ATTACH_VIRTUAL_DISK_PARAMETERS
title: ATTACH_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
author: windows-sdk-content
description: Contains virtual hard disk (VHD) attach request parameters.
old-location: vhd\attach_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 2bccad87-ddfe-4db4-9bf3-1892d8dd1237
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PATTACH_VIRTUAL_DISK_PARAMETERS, ATTACH_VIRTUAL_DISK_PARAMETERS, ATTACH_VIRTUAL_DISK_PARAMETERS structure [VHD], PATTACH_VIRTUAL_DISK_PARAMETERS, PATTACH_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _ATTACH_VIRTUAL_DISK_PARAMETERS, vdssys/ATTACH_VIRTUAL_DISK_PARAMETERS, vdssys/PATTACH_VIRTUAL_DISK_PARAMETERS, vhd.attach_virtual_disk_parameters, vhd.surface_virtual_disk_parameters, virtdisk/ATTACH_VIRTUAL_DISK_PARAMETERS, virtdisk/PATTACH_VIRTUAL_DISK_PARAMETERS"
ms.topic: struct
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - ATTACH_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.typenames: ATTACH_VIRTUAL_DISK_PARAMETERS, *PATTACH_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
---

# ATTACH_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD)  attach request parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/en-us/library/Dd323695(v=VS.85).aspx">ATTACH_VIRTUAL_DISK_VERSION</a> 
     enumeration that specifies the version of the 
     <b>ATTACH_VIRTUAL_DISK_PARAMETERS</b> 
     structure being passed to or from the VHD functions.


### -field Version1

A structure with the following member.


### -field Version1.Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

