---
UID: NE:vds._VDS_VOLUME_PLEX_TYPE
title: VDS_VOLUME_PLEX_TYPE (vds.h)
description: Defines the set of valid types for a volume plex.
helpviewer_keywords: ["VDS_VOLUME_PLEX_TYPE","VDS_VOLUME_PLEX_TYPE enumeration [VDS]","VDS_VPT_PARITY","VDS_VPT_SIMPLE","VDS_VPT_SPAN","VDS_VPT_STRIPE","VDS_VPT_UNKNOWN","base.vds_volume_plex_type","vds/VDS_VOLUME_PLEX_TYPE","vds/VDS_VPT_PARITY","vds/VDS_VPT_SIMPLE","vds/VDS_VPT_SPAN","vds/VDS_VPT_STRIPE","vds/VDS_VPT_UNKNOWN"]
old-location: base\vds_volume_plex_type.htm
tech.root: base
ms.assetid: b0cd0418-35fa-40ff-964b-154c7f01f4df
ms.date: 12/05/2018
ms.keywords: VDS_VOLUME_PLEX_TYPE, VDS_VOLUME_PLEX_TYPE enumeration [VDS], VDS_VPT_PARITY, VDS_VPT_SIMPLE, VDS_VPT_SPAN, VDS_VPT_STRIPE, VDS_VPT_UNKNOWN, base.vds_volume_plex_type, vds/VDS_VOLUME_PLEX_TYPE, vds/VDS_VPT_PARITY, vds/VDS_VPT_SIMPLE, vds/VDS_VPT_SPAN, vds/VDS_VPT_STRIPE, vds/VDS_VPT_UNKNOWN
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
req.typenames: VDS_VOLUME_PLEX_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_PLEX_TYPE
 - vds/_VDS_VOLUME_PLEX_TYPE
 - VDS_VOLUME_PLEX_TYPE
 - vds/VDS_VOLUME_PLEX_TYPE
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
 - VDS_VOLUME_PLEX_TYPE
---

# VDS_VOLUME_PLEX_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for a volume plex.

## -enum-fields

### -field VDS_VPT_UNKNOWN:0

This value is reserved.

### -field VDS_VPT_SIMPLE

The plex type is simple—it is composed of extents from exactly one disk. This value corresponds to the <b>VDS_VT_SIMPLE</b> value of the <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration.

### -field VDS_VPT_SPAN

The plex type is spanned—it is composed of extents from more than one disk. This value corresponds to the <b>VDS_VT_SPAN</b> value of the <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration.

### -field VDS_VPT_STRIPE

The plex type is striped, which is equivalent to RAID 0. This value corresponds to the <b>VDS_VT_STRIPE</b> value of the <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration.

### -field VDS_VPT_PARITY

The plex type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6. This value corresponds to the <b>VDS_VT_PARITY</b> value of the <a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a> enumeration.

## -remarks

The <a href="/windows/desktop/api/vds/ns-vds-vds_volume_plex_prop">VDS_VOLUME_PLEX_PROP</a> structure includes a <b>VDS_VOLUME_PLEX_TYPE</b> value as a member to indicate the existing plex type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_PLEX_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_PLEX_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_plex_prop">VDS_VOLUME_PLEX_PROP</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_type">VDS_VOLUME_TYPE</a>
