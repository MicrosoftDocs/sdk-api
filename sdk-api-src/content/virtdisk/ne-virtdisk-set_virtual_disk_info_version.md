---
UID: NE:virtdisk._SET_VIRTUAL_DISK_INFO_VERSION
title: SET_VIRTUAL_DISK_INFO_VERSION (virtdisk.h)
description: Contains the version of the virtual disk SET_VIRTUAL_DISK_INFO structure to use in calls to VHD functions.
helpviewer_keywords: ["SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE","SET_VIRTUAL_DISK_INFO_IDENTIFIER","SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR","SET_VIRTUAL_DISK_INFO_PARENT_PATH","SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH","SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE","SET_VIRTUAL_DISK_INFO_UNSPECIFIED","SET_VIRTUAL_DISK_INFO_VERSION","SET_VIRTUAL_DISK_INFO_VERSION enumeration [VHD]","SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID","vdssys/SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE","vdssys/SET_VIRTUAL_DISK_INFO_IDENTIFIER","vdssys/SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR","vdssys/SET_VIRTUAL_DISK_INFO_PARENT_PATH","vdssys/SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH","vdssys/SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE","vdssys/SET_VIRTUAL_DISK_INFO_UNSPECIFIED","vdssys/SET_VIRTUAL_DISK_INFO_VERSION","vdssys/SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID","vhd.set_virtual_disk_info_version","virtdisk/SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE","virtdisk/SET_VIRTUAL_DISK_INFO_IDENTIFIER","virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR","virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_PATH","virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH","virtdisk/SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE","virtdisk/SET_VIRTUAL_DISK_INFO_UNSPECIFIED","virtdisk/SET_VIRTUAL_DISK_INFO_VERSION","virtdisk/SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID"]
old-location: vhd\set_virtual_disk_info_version.htm
tech.root: VStor
ms.assetid: c9dd9d64-f96b-48f0-bc85-2f81ea3e2cb5
ms.date: 12/05/2018
ms.keywords: SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, SET_VIRTUAL_DISK_INFO_IDENTIFIER, SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR, SET_VIRTUAL_DISK_INFO_PARENT_PATH, SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH, SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE, SET_VIRTUAL_DISK_INFO_UNSPECIFIED, SET_VIRTUAL_DISK_INFO_VERSION, SET_VIRTUAL_DISK_INFO_VERSION enumeration [VHD], SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID, vdssys/SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, vdssys/SET_VIRTUAL_DISK_INFO_IDENTIFIER, vdssys/SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR, vdssys/SET_VIRTUAL_DISK_INFO_PARENT_PATH, vdssys/SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH, vdssys/SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE, vdssys/SET_VIRTUAL_DISK_INFO_UNSPECIFIED, vdssys/SET_VIRTUAL_DISK_INFO_VERSION, vdssys/SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID, vhd.set_virtual_disk_info_version, virtdisk/SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE, virtdisk/SET_VIRTUAL_DISK_INFO_IDENTIFIER, virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR, virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_PATH, virtdisk/SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH, virtdisk/SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE, virtdisk/SET_VIRTUAL_DISK_INFO_UNSPECIFIED, virtdisk/SET_VIRTUAL_DISK_INFO_VERSION, virtdisk/SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID
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
targetos: Windows
req.typenames: SET_VIRTUAL_DISK_INFO_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SET_VIRTUAL_DISK_INFO_VERSION
 - virtdisk/_SET_VIRTUAL_DISK_INFO_VERSION
 - SET_VIRTUAL_DISK_INFO_VERSION
 - virtdisk/SET_VIRTUAL_DISK_INFO_VERSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - SET_VIRTUAL_DISK_INFO_VERSION
---

# SET_VIRTUAL_DISK_INFO_VERSION enumeration


## -description

Contains the version of the virtual disk 
    [SET_VIRTUAL_DISK_INFO](./ns-virtdisk-set_virtual_disk_info.md) structure to use in calls to 
    VHD functions. Use the different versions of the structure to set different kinds of information for the VHD.

## -enum-fields

### -field SET_VIRTUAL_DISK_INFO_UNSPECIFIED:0

Not used. Will fail the operation.

### -field SET_VIRTUAL_DISK_INFO_PARENT_PATH:1

Parent information is being set.

### -field SET_VIRTUAL_DISK_INFO_IDENTIFIER:2

A unique identifier is being set.

<div class="alert"><b>Note</b>  If the VHD's unique identifier changes as a result of the 
       <b>SET_VIRTUAL_DISK_INFO_IDENTIFIER</b> operation, it will break any existing differencing 
       chains on the VHD.</div>
<div> </div>

### -field SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH:3

Sets the parent file path and the child depth.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

### -field SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE:4

Sets the physical sector size reported by the VHD.

<b>Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

### -field SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID:5

The identifier that is uniquely created when a user first creates the virtual disk to attempt to uniquely identify that virtual disk. 

<b>Windows 8 and Windows Server 2012:  </b>This value is not supported before Windows 8.1 and Windows Server 2012 R2.

### -field SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE:6

Whether resilient change tracking (RCT) is turned on for the virtual disk.

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This value is not supported before Windows 10 and Windows Server 2016.

### -field SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR:7

The parent linkage information that differencing VHDs store. Parent linkage information is metadata used to locate and correctly identify the next parent in the virtual disk  chain. 

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This value is not supported before Windows 10 and Windows Server 2016.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
