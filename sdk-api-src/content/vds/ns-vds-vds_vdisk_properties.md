---
UID: NS:vds._VDS_VDISK_PROPERTIES
title: VDS_VDISK_PROPERTIES (vds.h)
description: Defines the properties of a virtual disk.
helpviewer_keywords: ["*PVDS_VDISK_PROPERTIES","PVDS_VDISK_PROPERTIES","PVDS_VDISK_PROPERTIES structure pointer","VDS_VDISK_PROPERTIES","VDS_VDISK_PROPERTIES structure","base.vds_vdisk_properties","vds/PVDS_VDISK_PROPERTIES","vds/VDS_VDISK_PROPERTIES"]
old-location: base\vds_vdisk_properties.htm
tech.root: base
ms.assetid: e4cdab29-2bb7-4754-9ac8-d6f088910b0d
ms.date: 12/05/2018
ms.keywords: '*PVDS_VDISK_PROPERTIES, PVDS_VDISK_PROPERTIES, PVDS_VDISK_PROPERTIES structure pointer, VDS_VDISK_PROPERTIES, VDS_VDISK_PROPERTIES structure, base.vds_vdisk_properties, vds/PVDS_VDISK_PROPERTIES, vds/VDS_VDISK_PROPERTIES'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_VDISK_PROPERTIES, *PVDS_VDISK_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VDISK_PROPERTIES
 - vds/_VDS_VDISK_PROPERTIES
 - PVDS_VDISK_PROPERTIES
 - vds/PVDS_VDISK_PROPERTIES
 - VDS_VDISK_PROPERTIES
 - vds/VDS_VDISK_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_VDISK_PROPERTIES
---

# VDS_VDISK_PROPERTIES structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a virtual disk.

## -struct-fields

### -field Id

Unique VDS-specific session identifier of the disk.

### -field State

A <a href="/windows/desktop/api/vds/ne-vds-vds_vdisk_state">VDS_VDISK_STATE</a> enumeration value that specifies the virtual disk state.

### -field VirtualDeviceType

A pointer to a <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure that specifies the storage device type of the virtual disk.

### -field VirtualSize

The size, in bytes, of the virtual disk.

### -field PhysicalSize

The on-disk size, in bytes, of the virtual disk backing file.

### -field pPath

A <b>NULL</b>-terminated wide-character string containing the name and directory path of the backing file for the virtual disk.

### -field pDeviceName

A <b>NULL</b>-terminated wide-character string containing the name and device path of the disk device object for the volume where the virtual disk resides.

### -field DiskFlag

A bitmask of <a href="/windows/win32/api/virtdisk/ne-virtdisk-dependent_disk_flag">DEPENDENT_DISK_FLAG</a> enumeration values that specify disk dependency information.

### -field bIsChild

<b>TRUE</b> if the virtual disk is a child virtual disk, or <b>FALSE</b> otherwise.

### -field pParentPath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a parent virtual disk object.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvdisk-getproperties">IVdsVDisk::GetProperties</a>