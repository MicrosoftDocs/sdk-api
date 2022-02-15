---
UID: NE:sdoias._IASOSTYPE
title: IASOSTYPE (sdoias.h)
description: The values of the IASOSTYPE enumeration type specify what type of operating system the client requesting authentication (SDO computer) is running.
helpviewer_keywords: ["*PIASOSTYPE","IASOSTYPE","IASOSTYPE enumeration [Network Policy Server]","PIASOSTYPE","PIASOSTYPE enumeration pointer [Network Policy Server]","SYSTEM_TYPE_NT4_SERVER","SYSTEM_TYPE_NT4_WORKSTATION","SYSTEM_TYPE_NT5_SERVER","SYSTEM_TYPE_NT5_WORKSTATION","SYSTEM_TYPE_NT6_SERVER","SYSTEM_TYPE_NT6_WORKSTATION","_sdo_iasostype","nps.SDO_iasostype","sdo.iasostype","sdoias/IASOSTYPE","sdoias/PIASOSTYPE","sdoias/SYSTEM_TYPE_NT4_SERVER","sdoias/SYSTEM_TYPE_NT4_WORKSTATION","sdoias/SYSTEM_TYPE_NT5_SERVER","sdoias/SYSTEM_TYPE_NT5_WORKSTATION","sdoias/SYSTEM_TYPE_NT6_SERVER","sdoias/SYSTEM_TYPE_NT6_WORKSTATION"]
old-location: nps\SDO_iasostype.htm
tech.root: Nps
ms.assetid: 83a3d4cf-e0ab-467a-8c5a-b7372c76cca3
ms.date: 12/05/2018
ms.keywords: '*PIASOSTYPE, IASOSTYPE, IASOSTYPE enumeration [Network Policy Server], PIASOSTYPE, PIASOSTYPE enumeration pointer [Network Policy Server], SYSTEM_TYPE_NT4_SERVER, SYSTEM_TYPE_NT4_WORKSTATION, SYSTEM_TYPE_NT5_SERVER, SYSTEM_TYPE_NT5_WORKSTATION, SYSTEM_TYPE_NT6_SERVER, SYSTEM_TYPE_NT6_WORKSTATION, _sdo_iasostype, nps.SDO_iasostype, sdo.iasostype, sdoias/IASOSTYPE, sdoias/PIASOSTYPE, sdoias/SYSTEM_TYPE_NT4_SERVER, sdoias/SYSTEM_TYPE_NT4_WORKSTATION, sdoias/SYSTEM_TYPE_NT5_SERVER, sdoias/SYSTEM_TYPE_NT5_WORKSTATION, sdoias/SYSTEM_TYPE_NT6_SERVER, sdoias/SYSTEM_TYPE_NT6_WORKSTATION'
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
req.typenames: IASOSTYPE, *PIASOSTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IASOSTYPE
 - sdoias/_IASOSTYPE
 - PIASOSTYPE
 - sdoias/PIASOSTYPE
 - IASOSTYPE
 - sdoias/IASOSTYPE
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
 - IASOSTYPE
---

# IASOSTYPE enumeration


## -description

The values of the <b>IASOSTYPE</b> enumeration type specify what type of operating system the client requesting authentication (SDO computer) is running.

## -enum-fields

### -field SYSTEM_TYPE_NT4_WORKSTATION:0

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

<a href="/windows/win32/api/sdoias/ne-sdoias-iasdomaintype">IASDOMAINTYPE</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getostype">ISdoMachine::GetOSType</a>
