---
UID: NE:vds._VDS_HBAPORT_STATUS
title: VDS_HBAPORT_STATUS (vds.h)
description: Defines the set of valid statuses for an HBA port.
helpviewer_keywords: ["VDS_HBAPORT_STATUS","VDS_HBAPORT_STATUS enumeration [VDS]","VDS_HPS_BYPASSED","VDS_HPS_DIAGNOSTICS","VDS_HPS_ERROR","VDS_HPS_LINKDOWN","VDS_HPS_LOOPBACK","VDS_HPS_OFFLINE","VDS_HPS_ONLINE","VDS_HPS_UNKNOWN","base.vds_hbaport_status","vds/VDS_HBAPORT_STATUS","vds/VDS_HPS_BYPASSED","vds/VDS_HPS_DIAGNOSTICS","vds/VDS_HPS_ERROR","vds/VDS_HPS_LINKDOWN","vds/VDS_HPS_LOOPBACK","vds/VDS_HPS_OFFLINE","vds/VDS_HPS_ONLINE","vds/VDS_HPS_UNKNOWN","vdshwprv/VDS_HBAPORT_STATUS","vdshwprv/VDS_HPS_BYPASSED","vdshwprv/VDS_HPS_DIAGNOSTICS","vdshwprv/VDS_HPS_ERROR","vdshwprv/VDS_HPS_LINKDOWN","vdshwprv/VDS_HPS_LOOPBACK","vdshwprv/VDS_HPS_OFFLINE","vdshwprv/VDS_HPS_ONLINE","vdshwprv/VDS_HPS_UNKNOWN"]
old-location: base\vds_hbaport_status.htm
tech.root: base
ms.assetid: 67ef9025-c929-476b-8644-7e085dff91c4
ms.date: 12/05/2018
ms.keywords: VDS_HBAPORT_STATUS, VDS_HBAPORT_STATUS enumeration [VDS], VDS_HPS_BYPASSED, VDS_HPS_DIAGNOSTICS, VDS_HPS_ERROR, VDS_HPS_LINKDOWN, VDS_HPS_LOOPBACK, VDS_HPS_OFFLINE, VDS_HPS_ONLINE, VDS_HPS_UNKNOWN, base.vds_hbaport_status, vds/VDS_HBAPORT_STATUS, vds/VDS_HPS_BYPASSED, vds/VDS_HPS_DIAGNOSTICS, vds/VDS_HPS_ERROR, vds/VDS_HPS_LINKDOWN, vds/VDS_HPS_LOOPBACK, vds/VDS_HPS_OFFLINE, vds/VDS_HPS_ONLINE, vds/VDS_HPS_UNKNOWN, vdshwprv/VDS_HBAPORT_STATUS, vdshwprv/VDS_HPS_BYPASSED, vdshwprv/VDS_HPS_DIAGNOSTICS, vdshwprv/VDS_HPS_ERROR, vdshwprv/VDS_HPS_LINKDOWN, vdshwprv/VDS_HPS_LOOPBACK, vdshwprv/VDS_HPS_OFFLINE, vdshwprv/VDS_HPS_ONLINE, vdshwprv/VDS_HPS_UNKNOWN
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
req.typenames: VDS_HBAPORT_STATUS
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_HBAPORT_STATUS
 - vds/_VDS_HBAPORT_STATUS
 - VDS_HBAPORT_STATUS
 - vds/VDS_HBAPORT_STATUS
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
 - VDS_HBAPORT_STATUS
---

# VDS_HBAPORT_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the set of valid statuses for an HBA port. These values are used in the 
   <b>status</b> member of the 
   <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a> structure. These states correspond to 
   the HBA_PORTSTATE values in the HBA API.

## -enum-fields

### -field VDS_HPS_UNKNOWN:1

The HBA port status is unknown.
     

HBA_PORTSTATE_UNKNOWN

### -field VDS_HPS_ONLINE:2

The HBA port is operational.
     

HBA_PORTSTATE_ONLINE

### -field VDS_HPS_OFFLINE:3

The HBA port has been set offline by a user.
     

HBA_PORTSTATE_OFFLINE

### -field VDS_HPS_BYPASSED:4

The HBA port is bypassed.
     

HBA_PORTSTATE_BYPASSED

### -field VDS_HPS_DIAGNOSTICS:5

The HBA port is in diagnostics mode.
     

HBA_PORTSTATE_DIAGNOSTICS

### -field VDS_HPS_LINKDOWN:6

The HBA port link is down.
     

HBA_PORTSTATE_LINKDOWN

### -field VDS_HPS_ERROR:7

The HBA port has an error.
     

HBA_PORTSTATE_ERROR

### -field VDS_HPS_LOOPBACK:8

The HBA port is loopback.
     

HBA_PORTSTATE_LOOPBACK

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>
