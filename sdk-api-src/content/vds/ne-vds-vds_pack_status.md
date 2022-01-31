---
UID: NE:vds._VDS_PACK_STATUS
title: VDS_PACK_STATUS (vds.h)
description: Defines the set of object status values for a pack.
helpviewer_keywords: ["VDS_PACK_STATUS","VDS_PACK_STATUS enumeration [VDS]","VDS_PS_OFFLINE","VDS_PS_ONLINE","VDS_PS_UNKNOWN","base.vds_pack_status","vds/VDS_PACK_STATUS","vds/VDS_PS_OFFLINE","vds/VDS_PS_ONLINE","vds/VDS_PS_UNKNOWN"]
old-location: base\vds_pack_status.htm
tech.root: base
ms.assetid: a83d01e6-1173-410c-b880-3bc957d3f7e9
ms.date: 12/05/2018
ms.keywords: VDS_PACK_STATUS, VDS_PACK_STATUS enumeration [VDS], VDS_PS_OFFLINE, VDS_PS_ONLINE, VDS_PS_UNKNOWN, base.vds_pack_status, vds/VDS_PACK_STATUS, vds/VDS_PS_OFFLINE, vds/VDS_PS_ONLINE, vds/VDS_PS_UNKNOWN
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
req.typenames: VDS_PACK_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PACK_STATUS
 - vds/_VDS_PACK_STATUS
 - VDS_PACK_STATUS
 - vds/VDS_PACK_STATUS
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
 - VDS_PACK_STATUS
---

# VDS_PACK_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a pack.

## -enum-fields

### -field VDS_PS_UNKNOWN:0

This value is reserved.

### -field VDS_PS_ONLINE:1

The pack is available.

### -field VDS_PS_OFFLINE:4

The pack is unavailable; the disks in the pack are not accessible.

## -remarks

The <a href="/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a> structure includes a <b>VDS_PACK_STATUS</b> value as a member to indicate the current status of a pack.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PACK_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PACK_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a>
