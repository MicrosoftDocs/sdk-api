---
UID: NS:vds._VDS_VOLUME_PROP
title: VDS_VOLUME_PROP (vds.h)
description: Defines the properties of a volume object.
helpviewer_keywords: ["*PVDS_VOLUME_PROP","PVDS_VOLUME_PROP","PVDS_VOLUME_PROP structure pointer [VDS]","VDS_VOLUME_PROP","VDS_VOLUME_PROP structure [VDS]","base.vds_volume_prop","vds/PVDS_VOLUME_PROP","vds/_VDS_VOLUME_PROP"]
old-location: base\vds_volume_prop.htm
tech.root: base
ms.assetid: 3628b312-f830-4a1c-beb7-ad002a94313c
ms.date: 12/05/2018
ms.keywords: '*PVDS_VOLUME_PROP, PVDS_VOLUME_PROP, PVDS_VOLUME_PROP structure pointer [VDS], VDS_VOLUME_PROP, VDS_VOLUME_PROP structure [VDS], base.vds_volume_prop, vds/PVDS_VOLUME_PROP, vds/_VDS_VOLUME_PROP'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_VOLUME_PROP, *PVDS_VOLUME_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_PROP
 - vds/_VDS_VOLUME_PROP
 - PVDS_VOLUME_PROP
 - vds/PVDS_VOLUME_PROP
 - VDS_VOLUME_PROP
 - vds/VDS_VOLUME_PROP
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
 - VDS_VOLUME_PROP
---

# VDS_VOLUME_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a <a href="/windows/desktop/VDS/volume-object">volume object</a>.

## -struct-fields

### -field id

The GUID of the volume.

### -field type

A <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration value that specifies the type of the volume. Volume types are simple, spanned, striped (RAID-0), mirrored, or striped with parity (RAID-5).

### -field status

A <a href="/windows/desktop/api/vds/ne-vds-vds_volume_status">VDS_VOLUME_STATUS</a> enumeration value that specifies the status of the volume.

### -field health

A  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the volume.

### -field TransitionState

A  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the volume.

### -field ullSize

The size of the volume, in bytes.

### -field ulFlags

A bitmask of <a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a> enumeration values that describe the volume.

### -field RecommendedFileSystemType

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a> enumeration value that specifies the preferred file system for the volume. Must be one of the following: VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, VDS_FST_UDF, VDS_FST_CDFS, or VDS_FST_UNKNOWN.

### -field pwszName

The name used to open a handle for the volume with the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. For example, \\?\GLOBALROOT\Device\HarddiskVolume1.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a> method returns this structure to report the properties of a <a href="/windows/desktop/VDS/volume-object">volume object</a>.

When a volume is offline, the <b>VDS_VF_PERMANENTLY_DISMOUNTED</b> flag is set in the <b>ulFlags</b> member of the <b>VDS_VOLUME_PROP</b> structure, and the <b>VDS_VS_OFFLINE</b> volume status value is also set in the <b>status</b> member of this structure.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop2">VDS_VOLUME_PROP2</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_status">VDS_VOLUME_STATUS</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a>