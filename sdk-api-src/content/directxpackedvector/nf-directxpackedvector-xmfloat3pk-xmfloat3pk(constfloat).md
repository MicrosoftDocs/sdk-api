---
UID: NF:directxpackedvector.XMFLOAT3PK.XMFLOAT3PK(constfloat)
title: XMFLOAT3PK::XMFLOAT3PK(const float) (directxpackedvector.h)
description: Initializes a new instance of XMFLOAT3PK from a three element float array argument.
helpviewer_keywords: ["XMFLOAT3PK","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK structure","XMFLOAT3PK structure [DirectX Math Support APIs]","XMFLOAT3PK constructor","XMFLOAT3PK.XMFLOAT3PK","XMFLOAT3PK.XMFLOAT3PK()","XMFLOAT3PK.XMFLOAT3PK(const float)","XMFLOAT3PK::XMFLOAT3PK","XMFLOAT3PK::XMFLOAT3PK(const float)","dxmath.xmfloat3pk_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: ea6c8c8f-371d-40b8-8377-ccc4f75b0cf4
ms.date: 05/06/2019
ms.keywords: XMFLOAT3PK, XMFLOAT3PK constructor [DirectX Math Support APIs], XMFLOAT3PK constructor [DirectX Math Support APIs],XMFLOAT3PK structure, XMFLOAT3PK structure [DirectX Math Support APIs],XMFLOAT3PK constructor, XMFLOAT3PK.XMFLOAT3PK, XMFLOAT3PK.XMFLOAT3PK(), XMFLOAT3PK.XMFLOAT3PK(const float), XMFLOAT3PK::XMFLOAT3PK, XMFLOAT3PK::XMFLOAT3PK(const float), dxmath.xmfloat3pk_ctor_1
req.header: directxpackedvector.h
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
req.namespace: DirectX::PackedVector
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMFLOAT3PK::XMFLOAT3PK
 - directxpackedvector/XMFLOAT3PK::XMFLOAT3PK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMFLOAT3PK.XMFLOAT3PK
---

# XMFLOAT3PK::XMFLOAT3PK(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> from a three element <code>float</code> array argument.

This constructor initializes a new instance of **XMFLOAT3PK** from a three element <code>float</code>  array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Three element floating point array containing the values used to initialize the three components of a new instance of **XMFLOAT3PK**.

## -remarks

Values contained in *pArray[0]* and *pArray[1]* are stored, respectively, in the x-component and the y-component of the new instance of **XMFLOAT3PK**.

The values obtained from *pArray[0]* and *pArray[1]* are transformed from the standard 32 bit floating point format (sign bit, 8 bit exponent, 23 bit mantissa), and stored as an 11 bit floating point format (5 bit exponent, 6 bit mantissa).

Value contained in *pArray[2]* is stored, in the Z-component the new instance of **XMFLOAT3PK**.
The value obtained from *pArray[2]* is transformed from the standard 32-bit floating point format (sign bit, 8 bit exponent, 23 bit mantissa), and stored as a 10 bit floating point format (5 bit exponent, 5 bit mantissa).

As no target formats do not support a sign bit, all member of *pArray* must be greater than zero.

Because of the change in floating point format during the instantiation of an instance of **XMFLOAT3PK** by this constructor, some loss of precision can be expected.

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>

<a href="/windows/desktop/dxmath/xmfloat3pk-ctor">XMFLOAT3PK Constructors</a>