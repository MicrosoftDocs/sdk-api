---
UID: NE:sdoias._DOMAINTYPE
title: "_DOMAINTYPE"
author: windows-driver-content
description: The values of the IASDOMAINTYPE enumeration type specify whether the SDO computer is part of a domain, and if so, what type of domain.
old-location: nps\SDO_iasdomaintype.htm
old-project: Nps
ms.assetid: d6c36f76-d265-446b-986e-b23d9550ba3b
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PIASDOMAINTYPE, DOMAIN_TYPE_MIXED, DOMAIN_TYPE_NONE, DOMAIN_TYPE_NT4, DOMAIN_TYPE_NT5, IASDOMAINTYPE, IASDOMAINTYPE enumeration [Network Policy Server], PIASDOMAINTYPE, PIASDOMAINTYPE enumeration pointer [Network Policy Server], _DOMAINTYPE, _sdo_iasdomaintype, nps.SDO_iasdomaintype, sdo.iasdomaintype, sdoias/DOMAIN_TYPE_MIXED, sdoias/DOMAIN_TYPE_NONE, sdoias/DOMAIN_TYPE_NT4, sdoias/DOMAIN_TYPE_NT5, sdoias/IASDOMAINTYPE, sdoias/PIASDOMAINTYPE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IASDOMAINTYPE, *PIASDOMAINTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SdoIas.h
api_name:
-	IASDOMAINTYPE
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DOMAINTYPE enumeration


## -description


The values of the 
<b>IASDOMAINTYPE</b> enumeration type specify whether the SDO computer is part of a domain, and if so, what type of domain.


## -enum-fields




### -field DOMAIN_TYPE_NONE

The SDO computer is running in stand-alone mode.


### -field DOMAIN_TYPE_NT4

Not supported.


### -field DOMAIN_TYPE_NT5

The SDO computer is part of a Windows domain running in native mode.


### -field DOMAIN_TYPE_MIXED

The SDO computer is part of a Windows domain running in mixed mode.


## -see-also




<a href="https://msdn.microsoft.com/83a3d4cf-e0ab-467a-8c5a-b7372c76cca3">IASOSTYPE</a>



<a href="https://msdn.microsoft.com/9c22ec67-4a12-4487-bac5-8f0e666b8029">ISdoMachine::GetDomainType</a>
 

 

