---
UID: NE:sdoias._DOMAINTYPE
title: IASDOMAINTYPE (sdoias.h)
description: The values of the IASDOMAINTYPE enumeration type specify whether the SDO computer is part of a domain, and if so, what type of domain.
helpviewer_keywords: ["*PIASDOMAINTYPE","DOMAIN_TYPE_MIXED","DOMAIN_TYPE_NONE","DOMAIN_TYPE_NT4","DOMAIN_TYPE_NT5","IASDOMAINTYPE","IASDOMAINTYPE enumeration [Network Policy Server]","PIASDOMAINTYPE","PIASDOMAINTYPE enumeration pointer [Network Policy Server]","_sdo_iasdomaintype","nps.SDO_iasdomaintype","sdo.iasdomaintype","sdoias/DOMAIN_TYPE_MIXED","sdoias/DOMAIN_TYPE_NONE","sdoias/DOMAIN_TYPE_NT4","sdoias/DOMAIN_TYPE_NT5","sdoias/IASDOMAINTYPE","sdoias/PIASDOMAINTYPE"]
old-location: nps\SDO_iasdomaintype.htm
tech.root: Nps
ms.assetid: d6c36f76-d265-446b-986e-b23d9550ba3b
ms.date: 12/05/2018
ms.keywords: '*PIASDOMAINTYPE, DOMAIN_TYPE_MIXED, DOMAIN_TYPE_NONE, DOMAIN_TYPE_NT4, DOMAIN_TYPE_NT5, IASDOMAINTYPE, IASDOMAINTYPE enumeration [Network Policy Server], PIASDOMAINTYPE, PIASDOMAINTYPE enumeration pointer [Network Policy Server], _sdo_iasdomaintype, nps.SDO_iasdomaintype, sdo.iasdomaintype, sdoias/DOMAIN_TYPE_MIXED, sdoias/DOMAIN_TYPE_NONE, sdoias/DOMAIN_TYPE_NT4, sdoias/DOMAIN_TYPE_NT5, sdoias/IASDOMAINTYPE, sdoias/PIASDOMAINTYPE'
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IASDOMAINTYPE, *PIASDOMAINTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOMAINTYPE
 - sdoias/_DOMAINTYPE
 - PIASDOMAINTYPE
 - sdoias/PIASDOMAINTYPE
 - IASDOMAINTYPE
 - sdoias/IASDOMAINTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASDOMAINTYPE
---

# IASDOMAINTYPE enumeration


## -description

The values of the 
<b>IASDOMAINTYPE</b> enumeration type specify whether the SDO computer is part of a domain, and if so, what type of domain.

## -enum-fields

### -field DOMAIN_TYPE_NONE:0

The SDO computer is running in stand-alone mode.

### -field DOMAIN_TYPE_NT4

Not supported.

### -field DOMAIN_TYPE_NT5

The SDO computer is part of a Windows domain running in native mode.

### -field DOMAIN_TYPE_MIXED

The SDO computer is part of a Windows domain running in mixed mode.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-iasostype">IASOSTYPE</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getdomaintype">ISdoMachine::GetDomainType</a>
