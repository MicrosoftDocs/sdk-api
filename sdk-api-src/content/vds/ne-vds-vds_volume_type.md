---
UID: NE:vds._VDS_VOLUME_TYPE
title: VDS_VOLUME_TYPE (vds.h)
description: Defines the set of valid types for a volume object.
helpviewer_keywords: ["VDS_VOLUME_TYPE","VDS_VOLUME_TYPE enumeration [VDS]","VDS_VT_MIRROR","VDS_VT_PARITY","VDS_VT_SIMPLE","VDS_VT_SPAN","VDS_VT_STRIPE","VDS_VT_UNKNOWN","base.vds_volume_type","vds/VDS_VOLUME_TYPE","vds/VDS_VT_MIRROR","vds/VDS_VT_PARITY","vds/VDS_VT_SIMPLE","vds/VDS_VT_SPAN","vds/VDS_VT_STRIPE","vds/VDS_VT_UNKNOWN"]
old-location: base\vds_volume_type.htm
tech.root: base
ms.assetid: 07a44bbf-0726-4094-9b5f-2d26b0030796
ms.date: 12/05/2018
ms.keywords: VDS_VOLUME_TYPE, VDS_VOLUME_TYPE enumeration [VDS], VDS_VT_MIRROR, VDS_VT_PARITY, VDS_VT_SIMPLE, VDS_VT_SPAN, VDS_VT_STRIPE, VDS_VT_UNKNOWN, base.vds_volume_type, vds/VDS_VOLUME_TYPE, vds/VDS_VT_MIRROR, vds/VDS_VT_PARITY, vds/VDS_VT_SIMPLE, vds/VDS_VT_SPAN, vds/VDS_VT_STRIPE, vds/VDS_VT_UNKNOWN
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
req.typenames: VDS_VOLUME_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_TYPE
 - vds/_VDS_VOLUME_TYPE
 - VDS_VOLUME_TYPE
 - vds/VDS_VOLUME_TYPE
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
 - VDS_VOLUME_TYPE
---

# VDS_VOLUME_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for a volume object.

## -enum-fields

### -field VDS_VT_UNKNOWN:0

The volume type is unknown.

### -field VDS_VT_SIMPLE:10

The volume type is simple—it is composed of extents from exactly one disk.

### -field VDS_VT_SPAN:11

The volume type is spanned—it is composed of extents from more than one disk.

### -field VDS_VT_STRIPE:12

The volume type is striped, which is equivalent to RAID 0.

### -field VDS_VT_MIRROR:13

The volume type is mirrored, which is equivalent to RAID 1.

### -field VDS_VT_PARITY:14

The volume type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6.

## -remarks

The  <a href="/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a> method passes a <b>VDS_VOLUME_TYPE</b> value as an argument to set a new volume type, and the <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure includes a <b>VDS_VOLUME_TYPE</b> value as a member to indicate  the existing volume type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a>
