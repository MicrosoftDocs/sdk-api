---
UID: NE:dxva9typ._COPP_BusType
title: COPP_BusType (dxva9typ.h)
description: Specifies the type of I/O bus used by the graphics adapter.
helpviewer_keywords: ["COPP_BusType","COPP_BusType","COPP_BusType enumeration [DirectShow]","COPP_BusTypeEnumeration","COPP_BusType_AGP","COPP_BusType_ForceDWORD","COPP_BusType_Integrated","COPP_BusType_PCI","COPP_BusType_PCIExpress","COPP_BusType_PCIX","COPP_BusType_Unknown","dshow.copp_bustype","dxva9typ/COPP_BusType","dxva9typ/COPP_BusType_AGP","dxva9typ/COPP_BusType_ForceDWORD","dxva9typ/COPP_BusType_Integrated","dxva9typ/COPP_BusType_PCI","dxva9typ/COPP_BusType_PCIExpress","dxva9typ/COPP_BusType_PCIX","dxva9typ/COPP_BusType_Unknown"]
old-location: dshow\copp_bustype.htm
tech.root: dshow
ms.assetid: eb3666bd-1987-419f-8d48-0dbca147bf7e
ms.date: 12/05/2018
ms.keywords: COPP_BusType, COPP_BusType , COPP_BusType enumeration [DirectShow], COPP_BusTypeEnumeration, COPP_BusType_AGP, COPP_BusType_ForceDWORD, COPP_BusType_Integrated, COPP_BusType_PCI, COPP_BusType_PCIExpress, COPP_BusType_PCIX, COPP_BusType_Unknown, dshow.copp_bustype, dxva9typ/COPP_BusType, dxva9typ/COPP_BusType_AGP, dxva9typ/COPP_BusType_ForceDWORD, dxva9typ/COPP_BusType_Integrated, dxva9typ/COPP_BusType_PCI, dxva9typ/COPP_BusType_PCIExpress, dxva9typ/COPP_BusType_PCIX, dxva9typ/COPP_BusType_Unknown
req.header: dxva9typ.h
req.include-header: Dxva.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: COPP_BusType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPP_BusType
 - dxva9typ/_COPP_BusType
 - COPP_BusType
 - dxva9typ/COPP_BusType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva9typ.h
api_name:
 - COPP_BusType
---

# COPP_BusType enumeration


## -description

Specifies the type of I/O bus used by the graphics adapter.

## -enum-fields

### -field COPP_BusType_Unknown:0

Unknown bus type.

### -field COPP_BusType_PCI:1

PCI bus.

### -field COPP_BusType_PCIX:2

PCI-X bus.

### -field COPP_BusType_PCIExpress:3

PCI Express bus.

### -field COPP_BusType_AGP:4

AGP bus.

### -field COPP_BusType_Integrated:0x80000000

Integrated bus. This flag can be combined with the other flags. This flag indicates that the command and status signals between the graphics adapter and other subsystems on the computer are not available on an expansion bus that has a public specification and standard connector type, unless it is a memory bus.

### -field COPP_BusType_ForceDWORD

Reserved.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
