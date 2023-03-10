---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateLookupTable3D
title: ID2D1DeviceContext2::CreateLookupTable3D (d2d1_3.h)
description: Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format. (ID2D1DeviceContext2.CreateLookupTable3D)
helpviewer_keywords: ["CreateLookupTable3D","CreateLookupTable3D method [Direct2D]","CreateLookupTable3D method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","CreateLookupTable3D method","ID2D1DeviceContext2.CreateLookupTable3D","ID2D1DeviceContext2::CreateLookupTable3D","d2d1_3/ID2D1DeviceContext2::CreateLookupTable3D","direct2d.id2d1devicecontext2_createlookuptable3d"]
old-location: direct2d\id2d1devicecontext2_createlookuptable3d.htm
tech.root: Direct2D
ms.assetid: 1c48804b-9876-9dbd-3d20-8a7b575fd3d8
ms.date: 12/05/2018
ms.keywords: CreateLookupTable3D, CreateLookupTable3D method [Direct2D], CreateLookupTable3D method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateLookupTable3D method, ID2D1DeviceContext2.CreateLookupTable3D, ID2D1DeviceContext2::CreateLookupTable3D, d2d1_3/ID2D1DeviceContext2::CreateLookupTable3D, direct2d.id2d1devicecontext2_createlookuptable3d
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext2::CreateLookupTable3D
 - d2d1_3/ID2D1DeviceContext2::CreateLookupTable3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext2.CreateLookupTable3D
---

# ID2D1DeviceContext2::CreateLookupTable3D


## -description

Creates a 3D lookup table for mapping a 3-channel input to a 3-channel output. The table data must be provided in 4-channel format.

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

An array containing two values.  The first value is the size in bytes from one row (X dimension) of LUT data to the next.  
          The second value is the size in bytes from one LUT data plane (X and Y dimensions) to the next.

### -param lookupTable [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d">ID2D1LookupTable3D</a>**</b>

Receives the new lookup table instance.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>
