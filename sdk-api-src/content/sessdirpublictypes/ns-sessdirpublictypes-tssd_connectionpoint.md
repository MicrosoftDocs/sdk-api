---
UID: NS:sessdirpublictypes.__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0002
title: TSSD_ConnectionPoint (sessdirpublictypes.h)
description: Defines the IP address of a target.
helpviewer_keywords: ["*PTSSD_ConnectionPoint","PTSSD_ConnectionPoint","PTSSD_ConnectionPoint structure pointer [Remote Desktop Services]","TSSD_ConnectionPoint","TSSD_ConnectionPoint structure [Remote Desktop Services]","sessdirpublictypes/PTSSD_ConnectionPoint","sessdirpublictypes/TSSD_ConnectionPoint","termserv.tssd_connectionpoint"]
old-location: termserv\tssd_connectionpoint.htm
tech.root: TermServ
ms.assetid: 489d79ab-8a59-4789-9dca-df26018bf58c
ms.date: 12/05/2018
ms.keywords: '*PTSSD_ConnectionPoint, PTSSD_ConnectionPoint, PTSSD_ConnectionPoint structure pointer [Remote Desktop Services], TSSD_ConnectionPoint, TSSD_ConnectionPoint structure [Remote Desktop Services], sessdirpublictypes/PTSSD_ConnectionPoint, sessdirpublictypes/TSSD_ConnectionPoint, termserv.tssd_connectionpoint'
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0002
 - sessdirpublictypes/__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0002
 - PTSSD_ConnectionPoint
 - sessdirpublictypes/PTSSD_ConnectionPoint
 - TSSD_ConnectionPoint
 - sessdirpublictypes/TSSD_ConnectionPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - TSSD_ConnectionPoint
---

# TSSD_ConnectionPoint structure


## -description

Defines the IP address of a target.

## -struct-fields

### -field ServerAddressB

The server address.

### -field AddressType

A value of the <a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-tssd_addrv46type">TSSD_AddrV46Type</a> enumeration  that indicates the IP address type.

### -field PortNumber

The IP port number.

### -field AddressScope

The scope of the address.

## -see-also

<a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-tssd_addrv46type">TSSD_AddrV46Type</a>

