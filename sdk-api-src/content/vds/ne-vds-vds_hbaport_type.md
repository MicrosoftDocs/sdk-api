---
UID: NE:vds._VDS_HBAPORT_TYPE
title: VDS_HBAPORT_TYPE (vds.h)
description: Defines the set of valid types for an HBA port.
helpviewer_keywords: ["VDS_HBAPORT_TYPE","VDS_HBAPORT_TYPE enumeration [VDS]","VDS_HPT_EPORT","VDS_HPT_FLPORT","VDS_HPT_FPORT","VDS_HPT_GPORT","VDS_HPT_LPORT","VDS_HPT_NLPORT","VDS_HPT_NOTPRESENT","VDS_HPT_NPORT","VDS_HPT_OTHER","VDS_HPT_PTP","VDS_HPT_UNKNOWN","base.vds_hbaport_type","vds/VDS_HBAPORT_TYPE","vds/VDS_HPT_EPORT","vds/VDS_HPT_FLPORT","vds/VDS_HPT_FPORT","vds/VDS_HPT_GPORT","vds/VDS_HPT_LPORT","vds/VDS_HPT_NLPORT","vds/VDS_HPT_NOTPRESENT","vds/VDS_HPT_NPORT","vds/VDS_HPT_OTHER","vds/VDS_HPT_PTP","vds/VDS_HPT_UNKNOWN","vdshwprv/VDS_HBAPORT_TYPE","vdshwprv/VDS_HPT_EPORT","vdshwprv/VDS_HPT_FLPORT","vdshwprv/VDS_HPT_FPORT","vdshwprv/VDS_HPT_GPORT","vdshwprv/VDS_HPT_LPORT","vdshwprv/VDS_HPT_NLPORT","vdshwprv/VDS_HPT_NOTPRESENT","vdshwprv/VDS_HPT_NPORT","vdshwprv/VDS_HPT_OTHER","vdshwprv/VDS_HPT_PTP","vdshwprv/VDS_HPT_UNKNOWN"]
old-location: base\vds_hbaport_type.htm
tech.root: base
ms.assetid: fcad33c0-9a85-4180-b5de-fbef06e9e6e6
ms.date: 12/05/2018
ms.keywords: VDS_HBAPORT_TYPE, VDS_HBAPORT_TYPE enumeration [VDS], VDS_HPT_EPORT, VDS_HPT_FLPORT, VDS_HPT_FPORT, VDS_HPT_GPORT, VDS_HPT_LPORT, VDS_HPT_NLPORT, VDS_HPT_NOTPRESENT, VDS_HPT_NPORT, VDS_HPT_OTHER, VDS_HPT_PTP, VDS_HPT_UNKNOWN, base.vds_hbaport_type, vds/VDS_HBAPORT_TYPE, vds/VDS_HPT_EPORT, vds/VDS_HPT_FLPORT, vds/VDS_HPT_FPORT, vds/VDS_HPT_GPORT, vds/VDS_HPT_LPORT, vds/VDS_HPT_NLPORT, vds/VDS_HPT_NOTPRESENT, vds/VDS_HPT_NPORT, vds/VDS_HPT_OTHER, vds/VDS_HPT_PTP, vds/VDS_HPT_UNKNOWN, vdshwprv/VDS_HBAPORT_TYPE, vdshwprv/VDS_HPT_EPORT, vdshwprv/VDS_HPT_FLPORT, vdshwprv/VDS_HPT_FPORT, vdshwprv/VDS_HPT_GPORT, vdshwprv/VDS_HPT_LPORT, vdshwprv/VDS_HPT_NLPORT, vdshwprv/VDS_HPT_NOTPRESENT, vdshwprv/VDS_HPT_NPORT, vdshwprv/VDS_HPT_OTHER, vdshwprv/VDS_HPT_PTP, vdshwprv/VDS_HPT_UNKNOWN
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
req.typenames: VDS_HBAPORT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_HBAPORT_TYPE
 - vds/_VDS_HBAPORT_TYPE
 - VDS_HBAPORT_TYPE
 - vds/VDS_HBAPORT_TYPE
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
 - VDS_HBAPORT_TYPE
---

# VDS_HBAPORT_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   set of valid types for an HBA port. These types correspond to the HBA_PORTTYPE values in the HBA API.

## -enum-fields

### -field VDS_HPT_UNKNOWN:1

The port type is unknown.
     

HBA_PORTTYPE_UNKNOWN

### -field VDS_HPT_OTHER:2

The port type is another (undefined) type.
     

HBA_PORTTYPE_OTHER

### -field VDS_HPT_NOTPRESENT:3

The port type is not present.
     

HBA_PORTTYPE_NOTPRESENT

### -field VDS_HPT_NPORT:5

The port type is a fabric.
     

HBA_PORTTYPE_NPORT

### -field VDS_HPT_NLPORT:6

The port type is a public loop.
     

HBA_PORTTYPE_NLPORT

### -field VDS_HPT_FLPORT:7

The port type is a fabric on a loop.
     

HBA_PORTTYPE_FLPORT

### -field VDS_HPT_FPORT:8

The port type is a fabric port.
     

HBA_PORTTYPE_FPORT

### -field VDS_HPT_EPORT:9

The port type is a fabric expansion port.

### -field VDS_HPT_GPORT:10

The port type is a generic fabric port.

### -field VDS_HPT_LPORT:20

The port type is a private loop.
     

HBA_PORTTYPE_LPORT

### -field VDS_HPT_PTP:21

The port type is point-to-point.
     

HBA_PORTTYPE_PTP

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
