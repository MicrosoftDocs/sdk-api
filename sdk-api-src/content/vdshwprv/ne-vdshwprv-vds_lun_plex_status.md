---
UID: NE:vdshwprv._VDS_LUN_PLEX_STATUS
title: VDS_LUN_PLEX_STATUS (vdshwprv.h)
description: Defines the set of object status values for a LUN plex.
helpviewer_keywords: ["VDS_LPS_FAILED","VDS_LPS_NOT_READY","VDS_LPS_OFFLINE","VDS_LPS_ONLINE","VDS_LPS_UNKNOWN","VDS_LUN_PLEX_STATUS","VDS_LUN_PLEX_STATUS enumeration [VDS]","base.vds_lun_plex_status","vds/VDS_LPS_FAILED","vds/VDS_LPS_NOT_READY","vds/VDS_LPS_OFFLINE","vds/VDS_LPS_ONLINE","vds/VDS_LPS_UNKNOWN","vds/VDS_LUN_PLEX_STATUS","vdshwprv/VDS_LPS_FAILED","vdshwprv/VDS_LPS_NOT_READY","vdshwprv/VDS_LPS_OFFLINE","vdshwprv/VDS_LPS_ONLINE","vdshwprv/VDS_LPS_UNKNOWN","vdshwprv/VDS_LUN_PLEX_STATUS"]
old-location: base\vds_lun_plex_status.htm
tech.root: base
ms.assetid: 04eed033-45b3-42bc-a304-25525cddd085
ms.date: 12/05/2018
ms.keywords: VDS_LPS_FAILED, VDS_LPS_NOT_READY, VDS_LPS_OFFLINE, VDS_LPS_ONLINE, VDS_LPS_UNKNOWN, VDS_LUN_PLEX_STATUS, VDS_LUN_PLEX_STATUS enumeration [VDS], base.vds_lun_plex_status, vds/VDS_LPS_FAILED, vds/VDS_LPS_NOT_READY, vds/VDS_LPS_OFFLINE, vds/VDS_LPS_ONLINE, vds/VDS_LPS_UNKNOWN, vds/VDS_LUN_PLEX_STATUS, vdshwprv/VDS_LPS_FAILED, vdshwprv/VDS_LPS_NOT_READY, vdshwprv/VDS_LPS_OFFLINE, vdshwprv/VDS_LPS_ONLINE, vdshwprv/VDS_LPS_UNKNOWN, vdshwprv/VDS_LUN_PLEX_STATUS
req.header: vdshwprv.h
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
req.typenames: VDS_LUN_PLEX_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_PLEX_STATUS
 - vdshwprv/_VDS_LUN_PLEX_STATUS
 - VDS_LUN_PLEX_STATUS
 - vdshwprv/VDS_LUN_PLEX_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_LUN_PLEX_STATUS
---

# VDS_LUN_PLEX_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a LUN plex.

## -enum-fields

### -field VDS_LPS_UNKNOWN:0

This value is reserved.

### -field VDS_LPS_ONLINE:1

The plex is available.

### -field VDS_LPS_NOT_READY:2

The plex is busy.

### -field VDS_LPS_OFFLINE:4

The plex is unavailable.

### -field VDS_LPS_FAILED:5

The plex has failed.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_plex_prop">VDS_LUN_PLEX_PROP</a> structure includes a <b>VDS_LUN_PLEX_STATUS</b> value as a member to indicate the current status of the LUN plex.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_PLEX_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_PLEX_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_plex_prop">VDS_LUN_PLEX_PROP</a>
