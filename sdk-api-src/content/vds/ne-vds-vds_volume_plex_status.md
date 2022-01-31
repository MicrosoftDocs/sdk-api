---
UID: NE:vds._VDS_VOLUME_PLEX_STATUS
title: VDS_VOLUME_PLEX_STATUS (vds.h)
description: Defines the set of object status values for a volume plex.
helpviewer_keywords: ["VDS_VOLUME_PLEX_STATUS","VDS_VOLUME_PLEX_STATUS enumeration [VDS]","VDS_VPS_FAILED","VDS_VPS_NO_MEDIA","VDS_VPS_ONLINE","VDS_VPS_UNKNOWN","base.vds_volume_plex_status","vds/VDS_VOLUME_PLEX_STATUS","vds/VDS_VPS_FAILED","vds/VDS_VPS_NO_MEDIA","vds/VDS_VPS_ONLINE","vds/VDS_VPS_UNKNOWN"]
old-location: base\vds_volume_plex_status.htm
tech.root: base
ms.assetid: 2e382a68-876a-4287-a7df-d7eadd8ce037
ms.date: 12/05/2018
ms.keywords: VDS_VOLUME_PLEX_STATUS, VDS_VOLUME_PLEX_STATUS enumeration [VDS], VDS_VPS_FAILED, VDS_VPS_NO_MEDIA, VDS_VPS_ONLINE, VDS_VPS_UNKNOWN, base.vds_volume_plex_status, vds/VDS_VOLUME_PLEX_STATUS, vds/VDS_VPS_FAILED, vds/VDS_VPS_NO_MEDIA, vds/VDS_VPS_ONLINE, vds/VDS_VPS_UNKNOWN
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
req.typenames: VDS_VOLUME_PLEX_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_VOLUME_PLEX_STATUS
 - vds/_VDS_VOLUME_PLEX_STATUS
 - VDS_VOLUME_PLEX_STATUS
 - vds/VDS_VOLUME_PLEX_STATUS
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
 - VDS_VOLUME_PLEX_STATUS
---

# VDS_VOLUME_PLEX_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a volume plex.

## -enum-fields

### -field VDS_VPS_UNKNOWN:0

This value is reserved.

### -field VDS_VPS_ONLINE:1

The volume plex is available.

### -field VDS_VPS_NO_MEDIA:3

The volume plex has no media.

### -field VDS_VPS_FAILED:5

The volume plex is unavailable.

## -remarks

The  <a href="/windows/desktop/api/vds/ns-vds-vds_volume_plex_prop">VDS_VOLUME_PLEX_PROP</a> structure includes a <b>VDS_VOLUME_PLEX_STATUS</b> value as a member to indicate the status of a volume plex.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_PLEX_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_PLEX_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_plex_prop">VDS_VOLUME_PLEX_PROP</a>
