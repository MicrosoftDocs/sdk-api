---
UID: NS:dxva2api._DXVA2_ValueRange
title: DXVA2_ValueRange (dxva2api.h)
description: Defines the range of supported values for a DirectX Video Acceleration (DXVA) operation.
helpviewer_keywords: ["DXVA2_ValueRange","DXVA2_ValueRange structure [Media Foundation]","dxva2api/DXVA2_ValueRange","e01328bb-9069-4874-aa35-b3c9bc1c6094","mf.dxva2_valuerange"]
old-location: mf\dxva2_valuerange.htm
tech.root: mf
ms.assetid: e01328bb-9069-4874-aa35-b3c9bc1c6094
ms.date: 12/05/2018
ms.keywords: DXVA2_ValueRange, DXVA2_ValueRange structure [Media Foundation], dxva2api/DXVA2_ValueRange, e01328bb-9069-4874-aa35-b3c9bc1c6094, mf.dxva2_valuerange
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVA2_ValueRange
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_ValueRange
 - dxva2api/_DXVA2_ValueRange
 - DXVA2_ValueRange
 - dxva2api/DXVA2_ValueRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_ValueRange
---

# DXVA2_ValueRange structure


## -description

Defines the range of supported values for a DirectX Video Acceleration (DXVA) operation.

## -struct-fields

### -field MinValue

Minimum supported value.

### -field MaxValue

Maximum supported value.

### -field DefaultValue

Default value.

### -field StepSize

Minimum increment between values.

## -remarks

All values in this structure are specified as <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_fixed32">DXVA2_Fixed32</a> structures.

## -see-also

<a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_fixed32">DXVA2_Fixed32</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>