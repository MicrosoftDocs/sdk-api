---
UID: NF:d2d1effectauthor_1.ID2D1EffectContext1.CreateLookupTable3D
title: ID2D1EffectContext1::CreateLookupTable3D (d2d1effectauthor_1.h)
description: Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format. (ID2D1EffectContext1.CreateLookupTable3D)
helpviewer_keywords: ["CreateLookupTable3D","CreateLookupTable3D method [Direct2D]","CreateLookupTable3D method [Direct2D]","ID2D1EffectContext1 interface","ID2D1EffectContext1 interface [Direct2D]","CreateLookupTable3D method","ID2D1EffectContext1.CreateLookupTable3D","ID2D1EffectContext1::CreateLookupTable3D","d2d1effectauthor_1/ID2D1EffectContext1::CreateLookupTable3D","direct2d.id2d1effectcontext1_createlookuptable3d"]
old-location: direct2d\id2d1effectcontext1_createlookuptable3d.htm
tech.root: Direct2D
ms.assetid: 410D6785-944D-4A64-887A-0BD4511127DF
ms.date: 12/05/2018
ms.keywords: CreateLookupTable3D, CreateLookupTable3D method [Direct2D], CreateLookupTable3D method [Direct2D],ID2D1EffectContext1 interface, ID2D1EffectContext1 interface [Direct2D],CreateLookupTable3D method, ID2D1EffectContext1.CreateLookupTable3D, ID2D1EffectContext1::CreateLookupTable3D, d2d1effectauthor_1/ID2D1EffectContext1::CreateLookupTable3D, direct2d.id2d1effectcontext1_createlookuptable3d
req.header: d2d1effectauthor_1.h
req.include-header: 
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
req.lib: D2D1.lib
req.dll: D2D1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext1::CreateLookupTable3D
 - d2d1effectauthor_1/ID2D1EffectContext1::CreateLookupTable3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.dll
api_name:
 - ID2D1EffectContext1.CreateLookupTable3D
---

# ID2D1EffectContext1::CreateLookupTable3D


## -description

Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output.
        The table data must be provided in 4-channel format.

## -parameters

### -param precision

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

Precision of the input lookup table data.

### -param extents [in]

Type: <b>const UINT32*</b>

Number of lookup table elements per dimension (X, Y, Z).

### -param data [in]

Type: <b>const BYTE*</b>

Buffer holding the lookup table data.

### -param dataCount

Type: <b>UINT32</b>

Size of the lookup table data buffer.

### -param strides [in]

Type: <b>const UINT32*</b>

An array containing two values. The first value is the size in bytes from one row (X dimension) of LUT data to the next. 
          The second value is the size in bytes from one LUT data plane (X and Y dimensions) to the next.

### -param lookupTable [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d">ID2D1LookupTable3D</a>**</b>

Receives the new lookup table instance.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor_1/nn-d2d1effectauthor_1-id2d1effectcontext1">ID2D1EffectContext1</a>
