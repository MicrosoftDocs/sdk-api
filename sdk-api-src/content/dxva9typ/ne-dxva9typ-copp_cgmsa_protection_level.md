---
UID: NE:dxva9typ._COPP_CGMSA_Protection_Level
title: COPP_CGMSA_Protection_Level (dxva9typ.h)
description: Specifies the CGMS-A protection level.
helpviewer_keywords: ["COPP_CGMSA_CopyFreely","COPP_CGMSA_CopyNever","COPP_CGMSA_CopyNoMore","COPP_CGMSA_CopyOneGeneration","COPP_CGMSA_Disabled","COPP_CGMSA_ForceDWORD","COPP_CGMSA_LevelMax","COPP_CGMSA_LevelMin","COPP_CGMSA_Protection_Level","COPP_CGMSA_Protection_Level","COPP_CGMSA_Protection_Level enumeration [DirectShow]","COPP_CGMSA_Protection_LevelEnumeration","COPP_CGMSA_RedistributionControlRequired","dshow.copp_cgmsa_protection_level","dxva9typ/COPP_CGMSA_CopyFreely","dxva9typ/COPP_CGMSA_CopyNever","dxva9typ/COPP_CGMSA_CopyNoMore","dxva9typ/COPP_CGMSA_CopyOneGeneration","dxva9typ/COPP_CGMSA_Disabled","dxva9typ/COPP_CGMSA_ForceDWORD","dxva9typ/COPP_CGMSA_LevelMax","dxva9typ/COPP_CGMSA_LevelMin","dxva9typ/COPP_CGMSA_Protection_Level","dxva9typ/COPP_CGMSA_RedistributionControlRequired"]
old-location: dshow\copp_cgmsa_protection_level.htm
tech.root: dshow
ms.assetid: 37b453fa-c976-4b13-b94a-1eebd8ecd44b
ms.date: 12/05/2018
ms.keywords: COPP_CGMSA_CopyFreely, COPP_CGMSA_CopyNever, COPP_CGMSA_CopyNoMore, COPP_CGMSA_CopyOneGeneration, COPP_CGMSA_Disabled, COPP_CGMSA_ForceDWORD, COPP_CGMSA_LevelMax, COPP_CGMSA_LevelMin, COPP_CGMSA_Protection_Level, COPP_CGMSA_Protection_Level , COPP_CGMSA_Protection_Level enumeration [DirectShow], COPP_CGMSA_Protection_LevelEnumeration, COPP_CGMSA_RedistributionControlRequired, dshow.copp_cgmsa_protection_level, dxva9typ/COPP_CGMSA_CopyFreely, dxva9typ/COPP_CGMSA_CopyNever, dxva9typ/COPP_CGMSA_CopyNoMore, dxva9typ/COPP_CGMSA_CopyOneGeneration, dxva9typ/COPP_CGMSA_Disabled, dxva9typ/COPP_CGMSA_ForceDWORD, dxva9typ/COPP_CGMSA_LevelMax, dxva9typ/COPP_CGMSA_LevelMin, dxva9typ/COPP_CGMSA_Protection_Level, dxva9typ/COPP_CGMSA_RedistributionControlRequired
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
req.typenames: COPP_CGMSA_Protection_Level
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPP_CGMSA_Protection_Level
 - dxva9typ/_COPP_CGMSA_Protection_Level
 - COPP_CGMSA_Protection_Level
 - dxva9typ/COPP_CGMSA_Protection_Level
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
 - COPP_CGMSA_Protection_Level
---

# COPP_CGMSA_Protection_Level enumeration


## -description

Specifies the CGMS-A protection level.

## -enum-fields

### -field COPP_CGMSA_Disabled:0

CGMS-A is disabled.

### -field COPP_CGMSA_LevelMin

Minimum CGMS-A level. Equivalent to <b>COPP_CGMSA_Disabled</b>.

### -field COPP_CGMSA_CopyFreely:1

The protection level is Copy Freely.

### -field COPP_CGMSA_CopyNoMore:2

The protection level is Copy No More.

### -field COPP_CGMSA_CopyOneGeneration:3

The protection level is Copy One Generation.

### -field COPP_CGMSA_CopyNever:4

The protection level is Copy Never.

### -field COPP_CGMSA_RedistributionControlRequired:0x08

Redistribution control (or <i>broadcast flag</i>) is required. This flag can be combined with the other flags.

### -field COPP_CGMSA_LevelMax

Maximum CGMS-A level.

### -field COPP_CGMSA_ForceDWORD:0x7fffffff

Reserved.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/using-certified-output-protection-protocol--copp">Using Certified Output Protection Protocol (COPP)</a>
