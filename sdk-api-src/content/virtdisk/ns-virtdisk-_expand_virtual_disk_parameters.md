---
UID: NS:virtdisk._EXPAND_VIRTUAL_DISK_PARAMETERS
title: "_EXPAND_VIRTUAL_DISK_PARAMETERS"
author: windows-sdk-content
description: Contains virtual disk expansion request parameters.
old-location: vhd\expand_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 8a8a4d1c-7dbc-4dfe-9f21-94a3370553b8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PEXPAND_VIRTUAL_DISK_PARAMETERS, EXPAND_VIRTUAL_DISK_PARAMETERS, EXPAND_VIRTUAL_DISK_PARAMETERS structure [VHD], PEXPAND_VIRTUAL_DISK_PARAMETERS, PEXPAND_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _EXPAND_VIRTUAL_DISK_PARAMETERS, vdssys/EXPAND_VIRTUAL_DISK_PARAMETERS, vdssys/PEXPAND_VIRTUAL_DISK_PARAMETERS, vhd.expand_virtual_disk_parameters, virtdisk/EXPAND_VIRTUAL_DISK_PARAMETERS, virtdisk/PEXPAND_VIRTUAL_DISK_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
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
 - EXPAND_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.typenames: EXPAND_VIRTUAL_DISK_PARAMETERS, *PEXPAND_VIRTUAL_DISK_PARAMETERS
req.redist: 
---

# _EXPAND_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual disk expansion request parameters.


## -struct-fields




### -field Version

An <a href="https://msdn.microsoft.com/28651993-81ad-4dfc-9c8b-3768fab5d3ae">EXPAND_VIRTUAL_DISK_VERSION</a> 
      enumeration value that specifies the version of the 
      <b>EXPAND_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the virtual disk functions.


### -field Version1

This structure is used if the <b>Version</b> member is 
       <b>EXPAND_VIRTUAL_DISK_VERSION_1</b> (1).


### -field Version1.NewSize

New size, in bytes, for the expansion request.


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

