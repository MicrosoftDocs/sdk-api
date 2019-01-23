---
UID: NE:virtdisk._VIRTUAL_DISK_ACCESS_MASK
title: VIRTUAL_DISK_ACCESS_MASK
author: windows-sdk-content
description: Contains the bitmask for specifying access rights to a virtual hard disk (VHD) or CD or DVD image file (ISO).
old-location: vhd\virtual_disk_access_mask.htm
tech.root: VStor
ms.assetid: 2b1f02ab-dc32-4af1-880b-73e7db8602be
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VIRTUAL_DISK_ACCESS_ALL, VIRTUAL_DISK_ACCESS_ATTACH_RO, VIRTUAL_DISK_ACCESS_ATTACH_RW, VIRTUAL_DISK_ACCESS_CREATE, VIRTUAL_DISK_ACCESS_DETACH, VIRTUAL_DISK_ACCESS_GET_INFO, VIRTUAL_DISK_ACCESS_MASK, VIRTUAL_DISK_ACCESS_MASK enumeration [VHD], VIRTUAL_DISK_ACCESS_METAOPS, VIRTUAL_DISK_ACCESS_NONE, VIRTUAL_DISK_ACCESS_READ, VIRTUAL_DISK_ACCESS_WRITABLE, vdssys/VIRTUAL_DISK_ACCESS_ALL, vdssys/VIRTUAL_DISK_ACCESS_ATTACH_RO, vdssys/VIRTUAL_DISK_ACCESS_ATTACH_RW, vdssys/VIRTUAL_DISK_ACCESS_CREATE, vdssys/VIRTUAL_DISK_ACCESS_DETACH, vdssys/VIRTUAL_DISK_ACCESS_GET_INFO, vdssys/VIRTUAL_DISK_ACCESS_MASK, vdssys/VIRTUAL_DISK_ACCESS_METAOPS, vdssys/VIRTUAL_DISK_ACCESS_NONE, vdssys/VIRTUAL_DISK_ACCESS_READ, vdssys/VIRTUAL_DISK_ACCESS_WRITABLE, vhd.virtual_disk_access_mask, virtdisk/VIRTUAL_DISK_ACCESS_ALL, virtdisk/VIRTUAL_DISK_ACCESS_ATTACH_RO, virtdisk/VIRTUAL_DISK_ACCESS_ATTACH_RW, virtdisk/VIRTUAL_DISK_ACCESS_CREATE, virtdisk/VIRTUAL_DISK_ACCESS_DETACH, virtdisk/VIRTUAL_DISK_ACCESS_GET_INFO, virtdisk/VIRTUAL_DISK_ACCESS_MASK, virtdisk/VIRTUAL_DISK_ACCESS_METAOPS, virtdisk/VIRTUAL_DISK_ACCESS_NONE, virtdisk/VIRTUAL_DISK_ACCESS_READ, virtdisk/VIRTUAL_DISK_ACCESS_WRITABLE
ms.topic: enum
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
 - VIRTUAL_DISK_ACCESS_MASK
product: Windows
targetos: Windows
req.typenames: VIRTUAL_DISK_ACCESS_MASK
req.redist: 
---

# VIRTUAL_DISK_ACCESS_MASK enumeration


## -description


Contains the bitmask for specifying access rights to a virtual hard disk (VHD) or CD or DVD image 
    file (ISO).


## -enum-fields




### -field VIRTUAL_DISK_ACCESS_NONE

Open the virtual disk with no access. This is the only supported value when calling 
       <a href="https://msdn.microsoft.com/en-us/library/Dd323659(v=VS.85).aspx">CreateVirtualDisk</a> and specifying  
       <b>CREATE_VIRTUAL_DISK_VERSION_2</b> in the 
       <i>VirtualDiskAccessMask</i> parameter.


### -field VIRTUAL_DISK_ACCESS_ATTACH_RO

Open the virtual disk for read-only attach access. The caller must have <b>READ</b> 
       access to the virtual disk image file.

If used in a request to open a virtual disk that is already open, the 
       other handles must be limited to either <b>VIRTUAL_DISK_ACCESS_DETACH</b> or 
       <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> access, otherwise the open request with this flag will 
       fail.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field VIRTUAL_DISK_ACCESS_ATTACH_RW

Open the virtual disk for read/write attaching access. The caller must have 
       <code>(READ | WRITE)</code> access to the virtual disk image file.

If used in a request to open a virtual disk that is already open, the other handles must be limited to either 
       <b>VIRTUAL_DISK_ACCESS_DETACH</b> or <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> 
       access, otherwise the open request with this flag will fail.

If the virtual disk is part of a differencing chain, the disk for this request cannot be less than the 
       <b>RWDepth</b> specified during the prior open request for that differencing chain.

This flag is not supported for ISO virtual disks.


### -field VIRTUAL_DISK_ACCESS_DETACH

Open the virtual disk to allow detaching of an attached virtual disk. The caller must have 
       <code>(FILE_READ_ATTRIBUTES | FILE_READ_DATA)</code> access to the 
       virtual disk image file.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field VIRTUAL_DISK_ACCESS_GET_INFO

Information retrieval access to the virtual disk. The caller must have <b>READ</b> 
       access to the virtual disk image file.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.


### -field VIRTUAL_DISK_ACCESS_CREATE

Virtual disk creation access.

This flag is not supported for ISO virtual disks.


### -field VIRTUAL_DISK_ACCESS_METAOPS

Open the virtual disk to perform offline meta-operations. The caller must have 
       <code>(READ | WRITE)</code> access to the virtual disk image file, up 
       to  <b>RWDepth</b> if working with a differencing chain.

If the virtual disk is part of a differencing chain, the backing store (host volume) is opened in RW 
       exclusive mode up to <b>RWDepth</b>.

This flag is not supported for ISO virtual disks.


### -field VIRTUAL_DISK_ACCESS_READ

Reserved.


### -field VIRTUAL_DISK_ACCESS_ALL

Allows unrestricted access to the virtual disk. The caller must have unrestricted access rights to the 
       virtual disk image file.

This flag is not supported for ISO virtual disks.


### -field VIRTUAL_DISK_ACCESS_WRITABLE

Reserved.

This flag is not supported for ISO virtual disks.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

