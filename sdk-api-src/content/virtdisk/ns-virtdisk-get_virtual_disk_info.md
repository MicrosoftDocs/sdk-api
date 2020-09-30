---
UID: NS:virtdisk._GET_VIRTUAL_DISK_INFO
title: GET_VIRTUAL_DISK_INFO (virtdisk.h)
description: Contains virtual hard disk (VHD) information.
helpviewer_keywords: ["*PGET_VIRTUAL_DISK_INFO","GET_VIRTUAL_DISK_INFO","GET_VIRTUAL_DISK_INFO structure [VHD]","PGET_VIRTUAL_DISK_INFO","PGET_VIRTUAL_DISK_INFO structure pointer [VHD]","_GET_VIRTUAL_DISK_INFO","vdssys/GET_VIRTUAL_DISK_INFO","vdssys/PGET_VIRTUAL_DISK_INFO","vhd.get_virtual_disk_info","virtdisk/GET_VIRTUAL_DISK_INFO","virtdisk/PGET_VIRTUAL_DISK_INFO"]
old-location: vhd\get_virtual_disk_info.htm
tech.root: VStor
ms.assetid: 666c1d6e-cf23-4452-98ea-e7d4c31c3d3b
ms.date: 12/05/2018
ms.keywords: '*PGET_VIRTUAL_DISK_INFO, GET_VIRTUAL_DISK_INFO, GET_VIRTUAL_DISK_INFO structure [VHD], PGET_VIRTUAL_DISK_INFO, PGET_VIRTUAL_DISK_INFO structure pointer [VHD], _GET_VIRTUAL_DISK_INFO, vdssys/GET_VIRTUAL_DISK_INFO, vdssys/PGET_VIRTUAL_DISK_INFO, vhd.get_virtual_disk_info, virtdisk/GET_VIRTUAL_DISK_INFO, virtdisk/PGET_VIRTUAL_DISK_INFO'
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
req.typenames: GET_VIRTUAL_DISK_INFO, *PGET_VIRTUAL_DISK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GET_VIRTUAL_DISK_INFO
 - virtdisk/_GET_VIRTUAL_DISK_INFO
 - PGET_VIRTUAL_DISK_INFO
 - virtdisk/PGET_VIRTUAL_DISK_INFO
 - GET_VIRTUAL_DISK_INFO
 - virtdisk/GET_VIRTUAL_DISK_INFO
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
 - GET_VIRTUAL_DISK_INFO
---

# GET_VIRTUAL_DISK_INFO structure


## -description

Contains virtual hard disk (VHD) information.

## -struct-fields

### -field Version

A value of the 
      <a href="/windows/win32/api/virtdisk/ne-virtdisk-get_virtual_disk_info_version">GET_VIRTUAL_DISK_INFO_VERSION</a> enumeration 
      that specifies the version of the 
      <b>GET_VIRTUAL_DISK_INFO</b> structure being passed to 
      or from the virtual disk functions. This determines what parts of this structure will be used.

### -field Size

A structure with the following members. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_SIZE</b>.

### -field Size.VirtualSize

Virtual size of the virtual disk, in bytes.

### -field Size.PhysicalSize

Physical size of the virtual disk on physical disk, in bytes.

### -field Size.BlockSize

Block size of the virtual disk, in bytes.

### -field Size.SectorSize

Sector size of the virtual disk, in bytes.

### -field Identifier

Unique identifier of the virtual disk. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_IDENTIFIER</b>.

### -field ParentLocation

A structure with the following members. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_PARENT_LOCATION</b>.

### -field ParentLocation.ParentResolved

Parent resolution. <b>TRUE</b> if the parent backing store was successfully resolved, 
        <b>FALSE</b> if not.

### -field ParentLocation.ParentLocationBuffer

If the <b>ParentResolved</b> member is <b>TRUE</b>, contains the 
         path of the parent backing store.

If the <b>ParentResolved</b> member is <b>FALSE</b>, contains all of 
         the parent paths present in the search list.

### -field ParentIdentifier

Unique identifier of the parent disk backing store. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_PARENT_IDENTIFIER</b>.

### -field ParentTimestamp

Internal time stamp of the parent disk backing store. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_PARENT_TIMESTAMP</b>.

### -field VirtualStorageType

<a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure containing 
       information about the type of virtual disk. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_VIRTUAL_STORAGE_TYPE</b>.

### -field ProviderSubtype

Provider-specific subtype. Set the <b>Version</b> member to 
       <b>GET_VIRTUAL_DISK_INFO_PROVIDER_SUBTYPE</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Fixed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Dynamically expandable (sparse).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Differencing.

</td>
</tr>
</table>

### -field Is4kAligned

Indicates whether the virtual disk is 4 KB aligned. Set the <b>Version</b> member to 
        <b>GET_VIRTUAL_DISK_INFO_IS_4K_ALIGNED</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field IsLoaded

Indicates whether the virtual disk is currently mounted and in use. <b>TRUE</b> if the virtual disk is currently mounted and in use; otherwise <b>FALSE</b>. Set the <b>Version</b> member to <b>GET_VIRTUAL_DISK_INFO_IS_LOADED</b>.

<b>Windows 8 and Windows Server 2012:  </b>This is not supported before Windows 8.1 and Windows Server 2012 R2.

### -field PhysicalDisk

Details about the physical disk on which the virtual disk resides. Set the 
        <b>Version</b> member to 
        <b>GET_VIRTUAL_DISK_INFO_PHYSICAL_DISK</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field PhysicalDisk.LogicalSectorSize

The logical sector size of the physical disk.

### -field PhysicalDisk.PhysicalSectorSize

The physical sector size of the physical disk.

### -field PhysicalDisk.IsRemote

Indicates whether the physical disk is remote.

### -field VhdPhysicalSectorSize

The physical sector size of the virtual disk. Set the <b>Version</b> member to 
        <b>GET_VIRTUAL_DISK_INFO_VHD_PHYSICAL_SECTOR_SIZE</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field SmallestSafeVirtualSize

The smallest safe minimum size of the virtual disk. Set the 
        <b>Version</b> member to 
        <b>GET_VIRTUAL_DISK_INFO_SMALLEST_SAFE_VIRTUAL_SIZE</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field FragmentationPercentage

The fragmentation level of the virtual disk. Set the 
        <b>Version</b> member to 
        <b>GET_VIRTUAL_DISK_INFO_FRAGMENTATION</b>.

<b>Windows 7 and Windows Server 2008 R2:  </b>This is not supported before Windows 8 and Windows Server 2012.

### -field VirtualDiskId

The identifier that is uniquely created when a user first creates the virtual disk to attempt to uniquely identify that virtual disk. Set the <b>Version</b> member to <b>GET_VIRTUAL_DISK_INFO_VIRTUAL_DISK_ID</b>.

<b>Windows 8 and Windows Server 2012:  </b>This is not supported before Windows 8.1 and Windows Server 2012 R2.

### -field ChangeTrackingState

The state of resilient change tracking (RCT) for the virtual disk. Set the <b>Version</b> member to <b>GET_VIRTUAL_DISK_INFO_CHANGE_TRACKING_STATE</b>.

<b>Windows 8.1 and Windows Server 2012 R2:  </b>This member is not supported before Windows 10 and Windows Server 2016.

### -field ChangeTrackingState.Enabled

Whether RCT is turned on. <b>TRUE</b> if RCT is turned on; otherwise <b>FALSE</b>.

### -field ChangeTrackingState.NewerChanges

Whether the virtual disk has changed since the change identified by the <b>MostRecentId</b> member occurred. <b>TRUE</b> if the virtual disk has changed since the change identified by the <b>MostRecentId</b> member occurred; otherwise <b>FALSE</b>.

### -field ChangeTrackingState.MostRecentId

The change tracking identifier for the change that identifies the state of the virtual disk that you want to use as the basis of comparison to determine whether the <b>NewerChanges</b> member reports new changes.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/ne-virtdisk-get_virtual_disk_info_version">GET_VIRTUAL_DISK_INFO_VERSION</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation">GetVirtualDiskInformation</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>