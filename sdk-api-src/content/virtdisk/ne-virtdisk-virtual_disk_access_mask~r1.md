---
UID: NE:virtdisk._VIRTUAL_DISK_ACCESS_MASK~r1
title: VIRTUAL_DISK_ACCESS_MASK
ms.date: 01/30/2019
ms.keywords: _VIRTUAL_DISK_ACCESS_MASK, VIRTUAL_DISK_ACCESS_MASK
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: virtdisk.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - _VIRTUAL_DISK_ACCESS_MASK
 - virtdisk/_VIRTUAL_DISK_ACCESS_MASK
 - VIRTUAL_DISK_ACCESS_MASK
 - virtdisk/VIRTUAL_DISK_ACCESS_MASK
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - virtdisk.h
api_name:
 - _VIRTUAL_DISK_ACCESS_MASK
 - VIRTUAL_DISK_ACCESS_MASK
---

# VIRTUAL_DISK_ACCESS_MASK enumeration


## -description

Contains the bitmask for specifying access rights to a virtual hard disk (VHD) or CD or DVD image 
    file (ISO).

## -enum-fields

### -field VIRTUAL_DISK_ACCESS_NONE:0x00000000

Open the virtual disk with no access. This is the only supported value when calling 
       <a href="/windows/desktop/api/vdssys/nf-vdssys-createvirtualdisk">CreateVirtualDisk</a> and specifying  
       <b>CREATE_VIRTUAL_DISK_VERSION_2</b> in the 
       <i>VirtualDiskAccessMask</i> parameter.

### -field VIRTUAL_DISK_ACCESS_ATTACH_RO:0x00010000

Open the virtual disk for read-only attach access. The caller must have <b>READ</b> 
       access to the virtual disk image file.

If used in a request to open a virtual disk that is already open, the 
       other handles must be limited to either <b>VIRTUAL_DISK_ACCESS_DETACH</b> or 
       <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> access, otherwise the open request with this flag will 
       fail.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field VIRTUAL_DISK_ACCESS_ATTACH_RW:0x00020000

Open the virtual disk for read/write attaching access. The caller must have 
       <code>(READ | WRITE)</code> access to the virtual disk image file.

If used in a request to open a virtual disk that is already open, the other handles must be limited to either 
       <b>VIRTUAL_DISK_ACCESS_DETACH</b> or <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> 
       access, otherwise the open request with this flag will fail.

If the virtual disk is part of a differencing chain, the disk for this request cannot be less than the 
       <b>RWDepth</b> specified during the prior open request for that differencing chain.

This flag is not supported for ISO virtual disks.

### -field VIRTUAL_DISK_ACCESS_DETACH:0x00040000

Open the virtual disk to allow detaching of an attached virtual disk. The caller must have 
       <code>(FILE_READ_ATTRIBUTES | FILE_READ_DATA)</code> access to the 
       virtual disk image file.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field VIRTUAL_DISK_ACCESS_GET_INFO:0x00080000

Information retrieval access to the virtual disk. The caller must have <b>READ</b> 
       access to the virtual disk image file.

<b>Windows 7 and Windows Server 2008 R2:  </b>This access right is not supported for opening ISO virtual disks until Windows 8 and 
        Windows Server 2012.

### -field VIRTUAL_DISK_ACCESS_CREATE:0x00100000

Virtual disk creation access.

This flag is not supported for ISO virtual disks.

### -field VIRTUAL_DISK_ACCESS_METAOPS:0x00200000

Open the virtual disk to perform offline meta-operations. The caller must have 
       <code>(READ | WRITE)</code> access to the virtual disk image file, up 
       to  <b>RWDepth</b> if working with a differencing chain.

If the virtual disk is part of a differencing chain, the backing store (host volume) is opened in RW 
       exclusive mode up to <b>RWDepth</b>.

This flag is not supported for ISO virtual disks.

### -field VIRTUAL_DISK_ACCESS_READ:0x000d0000

Reserved.

### -field VIRTUAL_DISK_ACCESS_ALL:0x003f0000

Allows unrestricted access to the virtual disk. The caller must have unrestricted access rights to the 
       virtual disk image file.

This flag is not supported for ISO virtual disks.

### -field VIRTUAL_DISK_ACCESS_WRITABLE:0x00320000

Reserved.

## -remarks

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>

<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
