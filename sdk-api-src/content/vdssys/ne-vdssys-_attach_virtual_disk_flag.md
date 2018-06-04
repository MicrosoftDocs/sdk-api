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

# _ATTACH_VIRTUAL_DISK_FLAG enumeration


## -description


Contains virtual disk attach request flags.


## -enum-fields




### -field ATTACH_VIRTUAL_DISK_FLAG_NONE

No flags. Use system defaults.

This enumeration value is not supported for ISO virtual disks. 
       <b>ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY</b> must be specified.


### -field ATTACH_VIRTUAL_DISK_FLAG_READ_ONLY

Attach the virtual disk as read-only.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_DRIVE_LETTER

No drive letters are assigned to the disk's volumes.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_PERMANENT_LIFETIME

Will decouple the virtual disk lifetime from that of the <i>VirtualDiskHandle</i>. The 
       virtual disk will be attached until the 
       <a href="https://msdn.microsoft.com/9b3874e1-e107-42f8-9ede-eb1eb6164ed2">DetachVirtualDisk</a> function is called, even if all 
       open handles to the virtual disk are closed.

<b>Windows 7 and Windows Server 2008 R2:  </b>This flag is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_LOCAL_HOST

Reserved.

This flag is not supported for ISO virtual disks.


### -field ATTACH_VIRTUAL_DISK_FLAG_NO_SECURITY_DESCRIPTOR


### -field ATTACH_VIRTUAL_DISK_FLAG_BYPASS_DEFAULT_ENCRYPTION_POLICY




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

