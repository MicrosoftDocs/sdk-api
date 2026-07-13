---
UID: NF:directxpackedvector.XMFLOAT3SE.XMFLOAT3SE(constfloat)
title: XMFLOAT3SE::XMFLOAT3SE(const float) (directxpackedvector.h)
description: Initializes a new instance of XMFLOAT3SE from a three element float array argument.
helpviewer_keywords: ["XMFLOAT3SE","XMFLOAT3SE constructor [DirectX Math Support APIs]","XMFLOAT3SE constructor [DirectX Math Support APIs]","XMFLOAT3SE structure","XMFLOAT3SE structure [DirectX Math Support APIs]","XMFLOAT3SE constructor","XMFLOAT3SE.XMFLOAT3SE","XMFLOAT3SE.XMFLOAT3SE()","XMFLOAT3SE.XMFLOAT3SE(const float)","XMFLOAT3SE::XMFLOAT3SE","XMFLOAT3SE::XMFLOAT3SE(const float)","dxmath.xmfloat3se_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: d5e56b5a-c54f-4957-885c-4c4f0b7af71b
ms.date: 05/06/2019
ms.keywords: XMFLOAT3SE, XMFLOAT3SE constructor [DirectX Math Support APIs], XMFLOAT3SE constructor [DirectX Math Support APIs],XMFLOAT3SE structure, XMFLOAT3SE structure [DirectX Math Support APIs],XMFLOAT3SE constructor, XMFLOAT3SE.XMFLOAT3SE, XMFLOAT3SE.XMFLOAT3SE(), XMFLOAT3SE.XMFLOAT3SE(const float), XMFLOAT3SE::XMFLOAT3SE, XMFLOAT3SE::XMFLOAT3SE(const float), dxmath.xmfloat3se_ctor_1
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
 - XMFLOAT3SE::XMFLOAT3SE
 - directxpackedvector/XMFLOAT3SE::XMFLOAT3SE
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
 - XMFLOAT3SE.XMFLOAT3SE
---

# XMFLOAT3SE::XMFLOAT3SE(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a> from a three element <code>float</code> array argument.

This constructor initializes a new instance of **XMFLOAT3SE** from a from a three element float array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Three element floating point array containing the values used to initialize the three components of a new instance of **XMFLOAT3SE**.

## -remarks

Values contained in *pArray[0]*, *pArray[1]* and *pArray[2]* are stored, respectively, in the x-component, the y-component, and the z-component of the new instance of **XMFLOAT3SE**.

The values obtained from the members of *pArray* are transformed from the standard 32 bit floating point format (sign bit, 8 bit exponent, 23 bit mantissa), and stored as a 14 bit floating point format (5 bit exponent, 9 bit mantissa).

As no target formats do not support a sign bit, all member of *pArray* must be greater than zero.

Because of the change in floating point format during the instantiation of an instance of **XMFLOAT3SE** by this constructor, some loss of precision can be expected.

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a>

<a href="/windows/desktop/dxmath/xmfloat3se-ctor">XMFLOAT3SE Constructors</a>