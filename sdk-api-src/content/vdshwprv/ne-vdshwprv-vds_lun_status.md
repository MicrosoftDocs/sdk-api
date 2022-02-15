---
UID: NE:vdshwprv._VDS_LUN_STATUS
title: VDS_LUN_STATUS (vdshwprv.h)
description: Defines the set of object status values for a LUN.
helpviewer_keywords: ["*PVDS_LUN_STATUS","VDS_LS_FAILED","VDS_LS_NOT_READY","VDS_LS_OFFLINE","VDS_LS_ONLINE","VDS_LS_UNKNOWN","VDS_LUN_STATUS","VDS_LUN_STATUS enumeration [VDS]","base.vds_lun_status","vds/VDS_LS_FAILED","vds/VDS_LS_NOT_READY","vds/VDS_LS_OFFLINE","vds/VDS_LS_ONLINE","vds/VDS_LS_UNKNOWN","vds/VDS_LUN_STATUS","vdshwprv/VDS_LS_FAILED","vdshwprv/VDS_LS_NOT_READY","vdshwprv/VDS_LS_OFFLINE","vdshwprv/VDS_LS_ONLINE","vdshwprv/VDS_LS_UNKNOWN","vdshwprv/VDS_LUN_STATUS"]
old-location: base\vds_lun_status.htm
tech.root: base
ms.assetid: dac82973-d8c0-430b-aeea-163af7d94d24
ms.date: 12/05/2018
ms.keywords: '*PVDS_LUN_STATUS, VDS_LS_FAILED, VDS_LS_NOT_READY, VDS_LS_OFFLINE, VDS_LS_ONLINE, VDS_LS_UNKNOWN, VDS_LUN_STATUS, VDS_LUN_STATUS enumeration [VDS], base.vds_lun_status, vds/VDS_LS_FAILED, vds/VDS_LS_NOT_READY, vds/VDS_LS_OFFLINE, vds/VDS_LS_ONLINE, vds/VDS_LS_UNKNOWN, vds/VDS_LUN_STATUS, vdshwprv/VDS_LS_FAILED, vdshwprv/VDS_LS_NOT_READY, vdshwprv/VDS_LS_OFFLINE, vdshwprv/VDS_LS_ONLINE, vdshwprv/VDS_LS_UNKNOWN, vdshwprv/VDS_LUN_STATUS'
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
req.typenames: VDS_LUN_STATUS, *PVDS_LUN_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_STATUS
 - vdshwprv/_VDS_LUN_STATUS
 - PVDS_LUN_STATUS
 - vdshwprv/PVDS_LUN_STATUS
 - VDS_LUN_STATUS
 - vdshwprv/VDS_LUN_STATUS
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
 - VDS_LUN_STATUS
---

# VDS_LUN_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a LUN.

## -enum-fields

### -field VDS_LS_UNKNOWN:0

This value is reserved.

### -field VDS_LS_ONLINE:1

The LUN is available.

### -field VDS_LS_NOT_READY:2

The LUN is busy.

### -field VDS_LS_OFFLINE:4

The LUN is unavailable.

### -field VDS_LS_FAILED:5

The LUN has failed.

## -remarks

The  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-setstatus">IVdsLun::SetStatus</a> method passes a <b>VDS_LUN_STATUS</b> value as an argument to set the status of a LUN, and the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_prop">VDS_LUN_PROP</a> structure includes a <b>VDS_LUN_STATUS</b> value as a member to indicate the current status.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-setstatus">IVdsLun::SetStatus</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_prop">VDS_LUN_PROP</a>
