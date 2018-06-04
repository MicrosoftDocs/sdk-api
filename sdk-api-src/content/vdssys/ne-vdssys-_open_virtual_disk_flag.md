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

# _OPEN_VIRTUAL_DISK_FLAG enumeration


## -description


Contains virtual hard disk (VHD) or CD or DVD image file (ISO) open request flags.


## -enum-fields




### -field OPEN_VIRTUAL_DISK_FLAG_NONE

No flag specified.


### -field OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS

Open the VHD file (backing store) without opening any differencing-chain parents. Used to correct broken 
       parent links.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE

Reserved.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_BOOT_DRIVE

Reserved.

This flag is not supported for ISO virtual disks.


### -field OPEN_VIRTUAL_DISK_FLAG_CACHED_IO

Indicates that the virtual disk should be opened in cached mode. By default the virtual disks are opened 
       using <b>FILE_FLAG_NO_BUFFERING</b> and 
       <b>FILE_FLAG_WRITE_THROUGH</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN

Indicates the VHD file is to be opened without opening any differencing-chain parents and the parent chain is 
       to be created manually using the 
       <a href="https://msdn.microsoft.com/1af2a21b-246e-42d0-a493-4c513e716dab">AddVirtualDiskParent</a> function.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field OPEN_VIRTUAL_DISK_FLAG_PARENT_CACHED_IO


### -field OPEN_VIRTUAL_DISK_FLAG_VHDSET_FILE_ONLY


### -field OPEN_VIRTUAL_DISK_FLAG_IGNORE_RELATIVE_PARENT_LOCATOR


### -field OPEN_VIRTUAL_DISK_FLAG_NO_WRITE_HARDENING




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

