---
UID: NE:virtdisk._GET_VIRTUAL_DISK_INFO_VERSION
title: GET_VIRTUAL_DISK_INFO_VERSION (virtdisk.h)

description: Contains the kinds of virtual hard disk (VHD) information that you can retrieve.
old-location: vhd\get_virtual_disk_info_version.htm
tech.root: VStor
ms.assetid: 603910e4-7568-4ddf-bd50-32a8a41bfca6

ms.date: 12/05/2018
ms.keywords: GET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, GET_VIRTUAL_DISK_INFO_FRAGMENTATION, GET_VIRTUAL_DISK_INFO_IDENTIFIER, GET_VIRTUAL_DISK_INFO_IS_4K_ALIGNED, GET_VIRTUAL_DISK_INFO_IS_LOADED, GET_VIRTUAL_DISK_INFO_PARENT_IDENTIFIER, GET_VIRTUAL_DISK_INFO_PARENT_LOCATION, GET_VIRTUAL_DISK_INFO_PARENT_TIMESTAMP, GET_VIRTUAL_DISK_INFO_PHYSICAL_DISK, GET_VIRTUAL_DISK_INFO_PROVIDER_SUBTYPE, GET_VIRTUAL_DISK_INFO_SIZE, GET_VIRTUAL_DISK_INFO_SMALLEST_SAFE_VIRTUAL_SIZE, GET_VIRTUAL_DISK_INFO_UNSPECIFIED, GET_VIRTUAL_DISK_INFO_VERSION, GET_VIRTUAL_DISK_INFO_VERSION enumeration [VHD], GET_VIRTUAL_DISK_INFO_VHD_PHYSICAL_SECTOR_SIZE, GET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID, GET_VIRTUAL_DISK_INFO_VIRTUAL_STORAGE_TYPE, vdssys/GET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, vdssys/GET_VIRTUAL_DISK_INFO_FRAGMENTATION, vdssys/GET_VIRTUAL_DISK_INFO_IDENTIFIER, vdssys/GET_VIRTUAL_DISK_INFO_IS_4K_ALIGNED, vdssys/GET_VIRTUAL_DISK_INFO_IS_LOADED, vdssys/GET_VIRTUAL_DISK_INFO_PARENT_IDENTIFIER, vdssys/GET_VIRTUAL_DISK_INFO_PARENT_LOCATION, vdssys/GET_VIRTUAL_DISK_INFO_PARENT_TIMESTAMP, vdssys/GET_VIRTUAL_DISK_INFO_PHYSICAL_DISK, vdssys/GET_VIRTUAL_DISK_INFO_PROVIDER_SUBTYPE, vdssys/GET_VIRTUAL_DISK_INFO_SIZE, vdssys/GET_VIRTUAL_DISK_INFO_SMALLEST_SAFE_VIRTUAL_SIZE, vdssys/GET_VIRTUAL_DISK_INFO_UNSPECIFIED, vdssys/GET_VIRTUAL_DISK_INFO_VERSION, vdssys/GET_VIRTUAL_DISK_INFO_VHD_PHYSICAL_SECTOR_SIZE, vdssys/GET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID, vdssys/GET_VIRTUAL_DISK_INFO_VIRTUAL_STORAGE_TYPE, vhd.get_virtual_disk_info_version, virtdisk/GET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, virtdisk/GET_VIRTUAL_DISK_INFO_FRAGMENTATION, virtdisk/GET_VIRTUAL_DISK_INFO_IDENTIFIER, virtdisk/GET_VIRTUAL_DISK_INFO_IS_4K_ALIGNED, virtdisk/GET_VIRTUAL_DISK_INFO_IS_LOADED, virtdisk/GET_VIRTUAL_DISK_INFO_PARENT_IDENTIFIER, virtdisk/GET_VIRTUAL_DISK_INFO_PARENT_LOCATION, virtdisk/GET_VIRTUAL_DISK_INFO_PARENT_TIMESTAMP, virtdisk/GET_VIRTUAL_DISK_INFO_PHYSICAL_DISK, virtdisk/GET_VIRTUAL_DISK_INFO_PROVIDER_SUBTYPE, virtdisk/GET_VIRTUAL_DISK_INFO_SIZE, virtdisk/GET_VIRTUAL_DISK_INFO_SMALLEST_SAFE_VIRTUAL_SIZE, virtdisk/GET_VIRTUAL_DISK_INFO_UNSPECIFIED, virtdisk/GET_VIRTUAL_DISK_INFO_VERSION, virtdisk/GET_VIRTUAL_DISK_INFO_VHD_PHYSICAL_SECTOR_SIZE, virtdisk/GET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID, virtdisk/GET_VIRTUAL_DISK_INFO_VIRTUAL_STORAGE_TYPE
ms.topic: enum
f1_keywords: 
 - "virtdisk/GET_VIRTUAL_DISK_INFO_VERSION"
dev_langs:
 - c++
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
 - GET_VIRTUAL_DISK_INFO_VERSION
targetos: Windows
req.typenames: GET_VIRTUAL_DISK_INFO_VERSION
req.redist: 
ms.custom: 19H1
---

# GET_VIRTUAL_DISK_INFO_VERSION enumeration


## -description


Contains the kinds of virtual hard disk (VHD) information that you can retrieve. For more information, 
    see [GET_VIRTUAL_DISK_INFO](/windows/win32/api/virtdisk/ns-virtdisk-get_virtual_disk_info)a>.


## -enum-fields




### -field GET_VIRTUAL_DISK_INFO_UNSPECIFIED

Reserved. This value should not be used.


### -field GET_VIRTUAL_DISK_INFO_SIZE

Information related to the virtual disk size, including total size, physical allocation used, block size, 
      and sector size.


### -field GET_VIRTUAL_DISK_INFO_IDENTIFIER

The unique identifier.  This identifier is persistently stored  in the virtual disk and will not change even 
      if the virtual disk file is copied to another file.


### -field GET_VIRTUAL_DISK_INFO_PARENT_LOCATION

The paths to parent virtual disks. Valid only for differencing virtual disks.


### -field GET_VIRTUAL_DISK_INFO_PARENT_IDENTIFIER

The unique identifier of the parent virtual disk. Valid only for differencing virtual disks.


### -field GET_VIRTUAL_DISK_INFO_PARENT_TIMESTAMP

The time stamp of the parent when the child virtual disk was created. Valid only for differencing virtual 
      disks.


### -field GET_VIRTUAL_DISK_INFO_VIRTUAL_STORAGE_TYPE

The device identifier and vendor identifier that identify the type of virtual disk.


### -field GET_VIRTUAL_DISK_INFO_PROVIDER_SUBTYPE

The type of virtual disk.


### -field GET_VIRTUAL_DISK_INFO_IS_4K_ALIGNED

Indicates whether the virtual disk is 4 KB aligned.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field GET_VIRTUAL_DISK_INFO_PHYSICAL_DISK

Details about the physical disk on which the virtual disk resides.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field GET_VIRTUAL_DISK_INFO_VHD_PHYSICAL_SECTOR_SIZE

The physical sector size of the virtual disk.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field GET_VIRTUAL_DISK_INFO_SMALLEST_SAFE_VIRTUAL_SIZE

The smallest safe minimum size of the virtual disk.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field GET_VIRTUAL_DISK_INFO_FRAGMENTATION

The fragmentation level of the virtual disk.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field GET_VIRTUAL_DISK_INFO_IS_LOADED

Whether the virtual disk is currently mounted and in use. 

<b>Windows 8 and Windows Server 2012:  </b>This value is not supported before Windows 8.1 and Windows Server 2012 R2.


### -field GET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID

The identifier that is uniquely created when a user first creates the virtual disk to attempt to uniquely identify that virtual disk. 

<b>Windows 8 and Windows Server 2012:  </b>This value is not supported before Windows 8.1 and Windows Server 2012 R2.


### -field GET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE

The state of resilient change tracking (RCT) for the virtual disk.

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This value is not supported before Windows 10 and Windows Server 2016.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



[GET_VIRTUAL_DISK_INFO](/windows/win32/api/virtdisk/ns-virtdisk-get_virtual_disk_info)a>



<a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation">GetVirtualDiskInformation</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
 

 

