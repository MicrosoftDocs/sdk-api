---
UID: NS:virtdisk._SET_VIRTUAL_DISK_INFO
title: SET_VIRTUAL_DISK_INFO (virtdisk.h)
description: Contains virtual hard disk (VHD) information to use when you call the SetVirtualDiskInformation function to set VHD properties.
helpviewer_keywords: ["*PSET_VIRTUAL_DISK_INFO","PSET_VIRTUAL_DISK_INFO","PSET_VIRTUAL_DISK_INFO structure pointer [VHD]","SET_VIRTUAL_DISK_INFO","SET_VIRTUAL_DISK_INFO structure [VHD]","_SET_VIRTUAL_DISK_INFO","vdssys/PSET_VIRTUAL_DISK_INFO","vdssys/SET_VIRTUAL_DISK_INFO","vhd.set_virtual_disk_info","virtdisk/PSET_VIRTUAL_DISK_INFO","virtdisk/SET_VIRTUAL_DISK_INFO"]
old-location: vhd\set_virtual_disk_info.htm
tech.root: VStor
ms.assetid: 04b2bb75-7905-469a-abf1-15591dc64686
ms.date: 12/05/2018
ms.keywords: '*PSET_VIRTUAL_DISK_INFO, PSET_VIRTUAL_DISK_INFO, PSET_VIRTUAL_DISK_INFO structure pointer [VHD], SET_VIRTUAL_DISK_INFO, SET_VIRTUAL_DISK_INFO structure [VHD], _SET_VIRTUAL_DISK_INFO, vdssys/PSET_VIRTUAL_DISK_INFO, vdssys/SET_VIRTUAL_DISK_INFO, vhd.set_virtual_disk_info, virtdisk/PSET_VIRTUAL_DISK_INFO, virtdisk/SET_VIRTUAL_DISK_INFO'
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
req.typenames: SET_VIRTUAL_DISK_INFO, *PSET_VIRTUAL_DISK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SET_VIRTUAL_DISK_INFO
 - virtdisk/_SET_VIRTUAL_DISK_INFO
 - PSET_VIRTUAL_DISK_INFO
 - virtdisk/PSET_VIRTUAL_DISK_INFO
 - SET_VIRTUAL_DISK_INFO
 - virtdisk/SET_VIRTUAL_DISK_INFO
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
 - SET_VIRTUAL_DISK_INFO
---

# SET_VIRTUAL_DISK_INFO structure


## -description

Contains virtual hard disk (VHD) information to use when you call the <a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation">SetVirtualDiskInformation</a> function to set VHD properties.

## -struct-fields

### -field Version

A <a href="/windows/win32/api/virtdisk/ne-virtdisk-set_virtual_disk_info_version">SET_VIRTUAL_DISK_INFO_VERSION</a> 
      enumeration that specifies the version of the 
      <b>SET_VIRTUAL_DISK_INFO</b> structure being passed to or 
      from the VHD functions. This determines the type of information set.

### -field ParentFilePath

The path to the parent backing store. Set the <b>Version</b> member to 
       <b>SET_VIRTUAL_DISK_INFO_PARENT_PATH</b> (1).

### -field UniqueIdentifier

The unique identifier of the VHD. Set the <b>Version</b> member to 
       <b>SET_VIRTUAL_DISK_INFO_IDENTIFIER</b> (2).

### -field ParentPathWithDepthInfo

Sets the parent file path and the child depth. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PARENT_PATH_WITH_DEPTH</b> (3).

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field ParentPathWithDepthInfo.ChildDepth

Specifies the depth to the child from the leaf. The leaf itself is at depth 1.

### -field ParentPathWithDepthInfo.ParentFilePath

Specifies the depth to the parent from the leaf. The leaf itself is at depth 1.

### -field VhdPhysicalSectorSize

Sets the physical sector size reported by the VHD. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PHYSICAL_SECTOR_SIZE</b> (4).<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field VirtualDiskId

The identifier that is uniquely created when a user first creates the  virtual disk to attempt to uniquely identify that virtual disk. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID</b> (5).

<b>Windows 8 and Windows Server 2012:  </b>This is not supported before Windows 8.1 and Windows Server 2012 R2.

### -field ChangeTrackingEnabled

Turns  resilient change tracking (RCT) on or off for the VHD. <b>TRUE</b> turns RCT on. <b>FALSE</b> turns RCT off. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE</b> (6).

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This member is not supported before Windows 10 and Windows Server 2016.

### -field ParentLocator

Sets the parent linkage information that differencing VHDs store. Parent linkage information is metadata used to locate and correctly identify the next parent in the virtual disk  chain. Set the <b>Version</b> member to 
        <b>SET_VIRTUAL_DISK_INFO_PARENT_LOCATOR</b> (7).

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This member is not supported before Windows 10 and Windows Server 2016.

### -field ParentLocator.LinkageId

The unique identifier for the parent linkage information.

### -field ParentLocator.ParentFilePath

The path of the file for the parent VHD.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>