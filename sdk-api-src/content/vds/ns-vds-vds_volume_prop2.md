---
UID: NS:vds._VDS_VOLUME_PROP2
title: VDS_VOLUME_PROP2 (vds.h)
description: Defines the properties of a volume object. This structure is identical to the VDS_VOLUME_PROP structure, except that it also includes the volume GUIDs.
helpviewer_keywords: ["*PVDS_VOLUME_PROP2","PVDS_VOLUME_PROP2","PVDS_VOLUME_PROP2 structure pointer","VDS_VOLUME_PROP2","VDS_VOLUME_PROP2 structure","base.vds_volume_prop2","vds/PVDS_VOLUME_PROP2","vds/VDS_VOLUME_PROP2"]
old-location: base\vds_volume_prop2.htm
tech.root: base
ms.assetid: e99aaead-f5ad-4181-9208-9158e9fac38f
ms.date: 12/05/2018
ms.keywords: '*PVDS_VOLUME_PROP2, PVDS_VOLUME_PROP2, PVDS_VOLUME_PROP2 structure pointer, VDS_VOLUME_PROP2, VDS_VOLUME_PROP2 structure, base.vds_volume_prop2, vds/PVDS_VOLUME_PROP2, vds/VDS_VOLUME_PROP2'
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
req.typenames: VDS_VOLUME_PROP2, *PVDS_VOLUME_PROP2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_PROP2
 - vds/_VDS_VOLUME_PROP2
 - PVDS_VOLUME_PROP2
 - vds/PVDS_VOLUME_PROP2
 - VDS_VOLUME_PROP2
 - vds/VDS_VOLUME_PROP2
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
 - VDS_VOLUME_PROP2
---

# VDS_VOLUME_PROP2 structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a <a href="/windows/desktop/VDS/volume-object">volume object</a>. This structure is identical to the <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure, except that it also includes the volume GUIDs.

## -struct-fields

### -field id

The GUID of the volume.

### -field type

A <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration value that specifies the volume type. Volume types are simple, spanned, striped (RAID-0), mirrored, or striped with parity (RAID-5).

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

### -field cbUniqueId

The length of the byte array that the <b>pUniqueId</b> member points to.

### -field pwszName

The name that was used to open a handle for the volume with the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. For example, \\?\GLOBALROOT\Device\HarddiskVolume1.

### -field pUniqueId

A byte array that contains the unique identifier for the volume.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume2-getproperties2">IVdsVolume2::GetProperties2</a> method returns this structure to report the properties of a <a href="/windows/desktop/VDS/volume-object">volume object</a>.

When a volume is offline, the <b>VDS_VF_PERMANENTLY_DISMOUNTED</b> flag is set in the <b>ulFlags</b> member of the <b>VDS_VOLUME_PROP2</b> structure, and the <b>VDS_VS_OFFLINE</b> volume status value is also set in the <b>status</b> member of this structure.

For GPT and dynamic volumes, the unique identifier that the <b>pUniqueId</b> member points to is globally unique.

For removable media drives, the volume exists and has its own unique identifier even if there is no media in the device. If a volume is formatted on removable media, that volume has its own unique identifier. For more information, see <a href="https://msdn.microsoft.com/library/ms802377.aspx">Supporting Mount Manager Requests in a Storage Class Driver</a>.

The format of the unique identifier may vary among different types of devices and volumes. For basic volumes on MBR disks, the unique identifier is based on the disk signature and partition offset. Because the disk signature and partition offset are DWORD values, the unique identifier cannot be guaranteed to be globally unique across computers.

If the disk signature changes, the volume's unique identifier also changes. Disk signature changes usually occur as a result of a collision during disk cloning.

Note that a unique identifier is not the same as a volume GUID path. To find the volume GUID paths for a volume, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf3-queryvolumeguidpathnames">IVdsVolumeMF3::QueryVolumeGuidPathnames</a> method.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume2-getproperties2">IVdsVolume2::GetProperties2</a>



<a href="https://msdn.microsoft.com/library/ms810149.aspx">MOUNTDEV_UNIQUE_ID</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_status">VDS_VOLUME_STATUS</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a>