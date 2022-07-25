---
UID: NE:vds._VDS_PATH_STATUS
title: VDS_PATH_STATUS (vds.h)
description: Defines the set of valid status values for a port.
helpviewer_keywords: ["VDS_MPS_FAILED","VDS_MPS_ONLINE","VDS_MPS_STANDBY","VDS_MPS_UNKNOWN","VDS_PATH_STATUS","VDS_PATH_STATUS enumeration [VDS]","base.vds_path_status","vds/VDS_MPS_FAILED","vds/VDS_MPS_ONLINE","vds/VDS_MPS_STANDBY","vds/VDS_MPS_UNKNOWN","vds/VDS_PATH_STATUS","vdshwprv/VDS_MPS_FAILED","vdshwprv/VDS_MPS_ONLINE","vdshwprv/VDS_MPS_STANDBY","vdshwprv/VDS_MPS_UNKNOWN","vdshwprv/VDS_PATH_STATUS"]
old-location: base\vds_path_status.htm
tech.root: base
ms.assetid: f0682db1-9058-4514-abb2-c10b936d4f41
ms.date: 12/05/2018
ms.keywords: VDS_MPS_FAILED, VDS_MPS_ONLINE, VDS_MPS_STANDBY, VDS_MPS_UNKNOWN, VDS_PATH_STATUS, VDS_PATH_STATUS enumeration [VDS], base.vds_path_status, vds/VDS_MPS_FAILED, vds/VDS_MPS_ONLINE, vds/VDS_MPS_STANDBY, vds/VDS_MPS_UNKNOWN, vds/VDS_PATH_STATUS, vdshwprv/VDS_MPS_FAILED, vdshwprv/VDS_MPS_ONLINE, vdshwprv/VDS_MPS_STANDBY, vdshwprv/VDS_MPS_UNKNOWN, vdshwprv/VDS_PATH_STATUS
req.header: vds.h
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
req.typenames: VDS_PATH_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PATH_STATUS
 - vds/_VDS_PATH_STATUS
 - VDS_PATH_STATUS
 - vds/VDS_PATH_STATUS
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
 - VDS_PATH_STATUS
---

# VDS_PATH_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
    the set of valid status values for a port.

## -enum-fields

### -field VDS_MPS_UNKNOWN:0

The path status is unknown.

### -field VDS_MPS_ONLINE:1

The path is active.

### -field VDS_MPS_FAILED:5

The path is failed.

### -field VDS_MPS_STANDBY:7

The path is in standby mode.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PATH_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PATH_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
