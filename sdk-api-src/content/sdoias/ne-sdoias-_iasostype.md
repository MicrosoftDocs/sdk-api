---
UID: NE:sdoias._IASOSTYPE
title: "_IASOSTYPE"
author: windows-driver-content
description: The values of the IASOSTYPE enumeration type specify what type of operating system the client requesting authentication (SDO computer) is running.
old-location: nps\SDO_iasostype.htm
old-project: Nps
ms.assetid: 83a3d4cf-e0ab-467a-8c5a-b7372c76cca3
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PIASOSTYPE, IASOSTYPE, IASOSTYPE enumeration [Network Policy Server], PIASOSTYPE, PIASOSTYPE enumeration pointer [Network Policy Server], SYSTEM_TYPE_NT4_SERVER, SYSTEM_TYPE_NT4_WORKSTATION, SYSTEM_TYPE_NT5_SERVER, SYSTEM_TYPE_NT5_WORKSTATION, SYSTEM_TYPE_NT6_SERVER, SYSTEM_TYPE_NT6_WORKSTATION, _IASOSTYPE, _sdo_iasostype, nps.SDO_iasostype, sdo.iasostype, sdoias/IASOSTYPE, sdoias/PIASOSTYPE, sdoias/SYSTEM_TYPE_NT4_SERVER, sdoias/SYSTEM_TYPE_NT4_WORKSTATION, sdoias/SYSTEM_TYPE_NT5_SERVER, sdoias/SYSTEM_TYPE_NT5_WORKSTATION, sdoias/SYSTEM_TYPE_NT6_SERVER, sdoias/SYSTEM_TYPE_NT6_WORKSTATION"
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
req.typenames: IASOSTYPE, *PIASOSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SdoIas.h
api_name:
-	IASOSTYPE
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _IASOSTYPE enumeration


## -description


The values of the <b>IASOSTYPE</b> enumeration type specify what type of operating system the client requesting authentication (SDO computer) is running.


## -enum-fields




### -field SYSTEM_TYPE_NT4_WORKSTATION

Not supported.


### -field SYSTEM_TYPE_NT5_WORKSTATION

Not supported.


### -field SYSTEM_TYPE_NT6_WORKSTATION

The SDO computer is running Windows Vista.


### -field SYSTEM_TYPE_NT6_1_WORKSTATION


### -field SYSTEM_TYPE_NT6_2_WORKSTATION


### -field SYSTEM_TYPE_NT6_3_WORKSTATION


### -field SYSTEM_TYPE_NT10_0_WORKSTATION


### -field SYSTEM_TYPE_NT4_SERVER

Not supported.


### -field SYSTEM_TYPE_NT5_SERVER

Not supported.


### -field SYSTEM_TYPE_NT6_SERVER

The SDO computer is running Windows Server 2008.


### -field SYSTEM_TYPE_NT6_1_SERVER


### -field SYSTEM_TYPE_NT6_2_SERVER


### -field SYSTEM_TYPE_NT6_3_SERVER


### -field SYSTEM_TYPE_NT10_0_SERVER




## -see-also




<a href="https://msdn.microsoft.com/d6c36f76-d265-446b-986e-b23d9550ba3b">IASDOMAINTYPE</a>



<a href="https://msdn.microsoft.com/aa4f31af-57b0-4ce2-b8b9-981e4ef30d31">ISdoMachine::GetOSType</a>
 

 

