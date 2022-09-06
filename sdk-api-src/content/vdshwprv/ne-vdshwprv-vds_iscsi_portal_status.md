---
UID: NE:vdshwprv._VDS_ISCSI_PORTAL_STATUS
title: VDS_ISCSI_PORTAL_STATUS (vdshwprv.h)
description: Defines the set of valid status values for an iSCSI portal.
helpviewer_keywords: ["VDS_IPS_FAILED","VDS_IPS_NOT_READY","VDS_IPS_OFFLINE","VDS_IPS_ONLINE","VDS_IPS_UNKNOWN","VDS_ISCSI_PORTAL_STATUS","VDS_ISCSI_PORTAL_STATUS enumeration [VDS]","base.vds_iscsi_portal_status","vds/VDS_IPS_FAILED","vds/VDS_IPS_NOT_READY","vds/VDS_IPS_OFFLINE","vds/VDS_IPS_ONLINE","vds/VDS_IPS_UNKNOWN","vds/VDS_ISCSI_PORTAL_STATUS","vdshwprv/VDS_IPS_FAILED","vdshwprv/VDS_IPS_NOT_READY","vdshwprv/VDS_IPS_OFFLINE","vdshwprv/VDS_IPS_ONLINE","vdshwprv/VDS_IPS_UNKNOWN","vdshwprv/VDS_ISCSI_PORTAL_STATUS"]
old-location: base\vds_iscsi_portal_status.htm
tech.root: base
ms.assetid: ae39dfb8-6519-4307-8038-3af670553f51
ms.date: 12/05/2018
ms.keywords: VDS_IPS_FAILED, VDS_IPS_NOT_READY, VDS_IPS_OFFLINE, VDS_IPS_ONLINE, VDS_IPS_UNKNOWN, VDS_ISCSI_PORTAL_STATUS, VDS_ISCSI_PORTAL_STATUS enumeration [VDS], base.vds_iscsi_portal_status, vds/VDS_IPS_FAILED, vds/VDS_IPS_NOT_READY, vds/VDS_IPS_OFFLINE, vds/VDS_IPS_ONLINE, vds/VDS_IPS_UNKNOWN, vds/VDS_ISCSI_PORTAL_STATUS, vdshwprv/VDS_IPS_FAILED, vdshwprv/VDS_IPS_NOT_READY, vdshwprv/VDS_IPS_OFFLINE, vdshwprv/VDS_IPS_ONLINE, vdshwprv/VDS_IPS_UNKNOWN, vdshwprv/VDS_ISCSI_PORTAL_STATUS
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VDS_ISCSI_PORTAL_STATUS
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_PORTAL_STATUS
 - vdshwprv/_VDS_ISCSI_PORTAL_STATUS
 - VDS_ISCSI_PORTAL_STATUS
 - vdshwprv/VDS_ISCSI_PORTAL_STATUS
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
 - VDS_ISCSI_PORTAL_STATUS
---

# VDS_ISCSI_PORTAL_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid status values for an iSCSI portal.

## -enum-fields

### -field VDS_IPS_UNKNOWN:0

The status is unknown.

### -field VDS_IPS_ONLINE:1

The portal is available.

### -field VDS_IPS_NOT_READY:2

The portal is busy.

### -field VDS_IPS_OFFLINE:4

The portal is unavailable.

### -field VDS_IPS_FAILED:5

The portal has failed.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_PORTAL_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_PORTAL_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setstatus">IVdsIscsiPortal::SetStatus</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portal_prop">VDS_ISCSI_PORTAL_PROP</a>
