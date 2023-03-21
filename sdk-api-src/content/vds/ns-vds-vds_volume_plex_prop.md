---
UID: NS:vds._VDS_VOLUME_PLEX_PROP
title: VDS_VOLUME_PLEX_PROP (vds.h)
description: Defines the properties of a volume plex object.
helpviewer_keywords: ["*PVDS_VOLUME_PLEX_PROP","PVDS_VOLUME_PLEX_PROP","PVDS_VOLUME_PLEX_PROP structure pointer [VDS]","VDS_VOLUME_PLEX_PROP","VDS_VOLUME_PLEX_PROP structure [VDS]","base.vds_volume_plex_prop","vds/PVDS_VOLUME_PLEX_PROP","vds/_VDS_VOLUME_PLEX_PROP"]
old-location: base\vds_volume_plex_prop.htm
tech.root: base
ms.assetid: 225cdc5e-045b-407f-b383-8f92025fbbd6
ms.date: 12/05/2018
ms.keywords: '*PVDS_VOLUME_PLEX_PROP, PVDS_VOLUME_PLEX_PROP, PVDS_VOLUME_PLEX_PROP structure pointer [VDS], VDS_VOLUME_PLEX_PROP, VDS_VOLUME_PLEX_PROP structure [VDS], base.vds_volume_plex_prop, vds/PVDS_VOLUME_PLEX_PROP, vds/_VDS_VOLUME_PLEX_PROP'
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
req.typenames: VDS_VOLUME_PLEX_PROP, *PVDS_VOLUME_PLEX_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_PLEX_PROP
 - vds/_VDS_VOLUME_PLEX_PROP
 - PVDS_VOLUME_PLEX_PROP
 - vds/PVDS_VOLUME_PLEX_PROP
 - VDS_VOLUME_PLEX_PROP
 - vds/VDS_VOLUME_PLEX_PROP
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
 - VDS_VOLUME_PLEX_PROP
---

# VDS_VOLUME_PLEX_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a <a href="/windows/desktop/VDS/volume-plex-object">volume plex object</a>.

## -struct-fields

### -field id

The GUID of the plex object.

### -field type

The plex type enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_volume_plex_type">VDS_VOLUME_PLEX_TYPE</a>. The type of the plex is not required to match the type of the volume to which the plex belongs.

### -field status

The status of the plex object enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_volume_plex_status">VDS_VOLUME_PLEX_STATUS</a>. The status of the plex is not required to match the status of the volume to which the plex belongs.

### -field health

A  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the plex.  The health state of the plex is not required to match the health state of the volume to which the plex belongs.

### -field TransitionState

A  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the plex.

### -field ullSize

The size of the plex, in bytes. The size of the plex must be greater than or equal to that of the volume to which the plex belongs. The plex cannot be smaller than the volume.

### -field ulStripeSize

The stripe interleave size, in bytes. This member is valid only for plexes of type <b>VDS_VPT_STRIPE</b> (striped) and <b>VDS_VPT_PARITY</b> (striped with parity). For other plex types, this member should be zero.

### -field ulNumberOfMembers

The number of members in the volume plex. A plex member is a collection of concatenated disk extents contained on one more disks.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-getproperties">IVdsVolumePlex::GetProperties</a> method returns this structure to report the properties of a <a href="/windows/desktop/VDS/volume-plex-object">volume plex object</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeplex-getproperties">IVdsVolumePlex::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_transition_state">VDS_TRANSITION_STATE</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_plex_status">VDS_VOLUME_PLEX_STATUS</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_plex_type">VDS_VOLUME_PLEX_TYPE</a>