---
UID: NS:virtdisk._COMPACT_VIRTUAL_DISK_PARAMETERS
title: "_COMPACT_VIRTUAL_DISK_PARAMETERS"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) compacting parameters.
old-location: vhd\compact_virtual_disk_parameters.htm
old-project: VStor
ms.assetid: 3e58101c-c8a9-432e-99c4-9e418a887b9e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: "*PCOMPACT_VIRTUAL_DISK_PARAMETERS, COMPACT_VIRTUAL_DISK_PARAMETERS, COMPACT_VIRTUAL_DISK_PARAMETERS structure [VHD], PCOMPACT_VIRTUAL_DISK_PARAMETERS, PCOMPACT_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _COMPACT_VIRTUAL_DISK_PARAMETERS, vhd.compact_virtual_disk_parameters, virtdisk/COMPACT_VIRTUAL_DISK_PARAMETERS, virtdisk/PCOMPACT_VIRTUAL_DISK_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: virtdisk.h
req.include-header: Windows.h
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
req.typenames: COMPACT_VIRTUAL_DISK_PARAMETERS, *PCOMPACT_VIRTUAL_DISK_PARAMETERS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	VirtDisk.h
api_name:
-	COMPACT_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _COMPACT_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD)  compacting parameters.


## -struct-fields




### -field Version

A <a href="https://msdn.microsoft.com/79b8088a-8e30-44c8-8227-82eb1c03e77c">COMPACT_VIRTUAL_DISK_VERSION</a> 
     enumeration that specifies the version of the 
     <b>COMPACT_VIRTUAL_DISK_PARAMETERS</b> 
     structure being passed to or from the VHD functions.


### -field Version1

A structure with the following member.


### -field Version1.Reserved

Reserved. Must be set to zero.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

