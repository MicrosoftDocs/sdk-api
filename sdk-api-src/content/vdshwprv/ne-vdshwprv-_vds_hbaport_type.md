---
UID: NE:vdshwprv._VDS_HBAPORT_TYPE
title: "_VDS_HBAPORT_TYPE"
author: windows-sdk-content
description: Defines the set of valid types for an HBA port.
old-location: base\vds_hbaport_type.htm
old-project: VDS
ms.assetid: fcad33c0-9a85-4180-b5de-fbef06e9e6e6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_HBAPORT_TYPE, VDS_HBAPORT_TYPE enumeration [VDS], VDS_HPT_EPORT, VDS_HPT_FLPORT, VDS_HPT_FPORT, VDS_HPT_GPORT, VDS_HPT_LPORT, VDS_HPT_NLPORT, VDS_HPT_NOTPRESENT, VDS_HPT_NPORT, VDS_HPT_OTHER, VDS_HPT_PTP, VDS_HPT_UNKNOWN, _VDS_HBAPORT_TYPE, base.vds_hbaport_type, vds/VDS_HBAPORT_TYPE, vds/VDS_HPT_EPORT, vds/VDS_HPT_FLPORT, vds/VDS_HPT_FPORT, vds/VDS_HPT_GPORT, vds/VDS_HPT_LPORT, vds/VDS_HPT_NLPORT, vds/VDS_HPT_NOTPRESENT, vds/VDS_HPT_NPORT, vds/VDS_HPT_OTHER, vds/VDS_HPT_PTP, vds/VDS_HPT_UNKNOWN, vdshwprv/VDS_HBAPORT_TYPE, vdshwprv/VDS_HPT_EPORT, vdshwprv/VDS_HPT_FLPORT, vdshwprv/VDS_HPT_FPORT, vdshwprv/VDS_HPT_GPORT, vdshwprv/VDS_HPT_LPORT, vdshwprv/VDS_HPT_NLPORT, vdshwprv/VDS_HPT_NOTPRESENT, vdshwprv/VDS_HPT_NPORT, vdshwprv/VDS_HPT_OTHER, vdshwprv/VDS_HPT_PTP, vdshwprv/VDS_HPT_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: VDS_HBAPORT_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_HBAPORT_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   set of valid types for an HBA port. These types correspond to the HBA_PORTTYPE values in the HBA API.


## -enum-fields




### -field VDS_HPT_UNKNOWN

The port type is unknown.
     

HBA_PORTTYPE_UNKNOWN


### -field VDS_HPT_OTHER

The port type is another (undefined) type.
     

HBA_PORTTYPE_OTHER


### -field VDS_HPT_NOTPRESENT

The port type is not present.
     

HBA_PORTTYPE_NOTPRESENT


### -field VDS_HPT_NPORT

The port type is a fabric.
     

HBA_PORTTYPE_NPORT


### -field VDS_HPT_NLPORT

The port type is a public loop.
     

HBA_PORTTYPE_NLPORT


### -field VDS_HPT_FLPORT

The port type is a fabric on a loop.
     

HBA_PORTTYPE_FLPORT


### -field VDS_HPT_FPORT

The port type is a fabric port.
     

HBA_PORTTYPE_FPORT


### -field VDS_HPT_EPORT

The port type is a fabric expansion port.
     




### -field VDS_HPT_GPORT

The port type is a generic fabric port.
     




### -field VDS_HPT_LPORT

The port type is a private loop.
     

HBA_PORTTYPE_LPORT


### -field VDS_HPT_PTP

The port type is point-to-point.
     

HBA_PORTTYPE_PTP


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

