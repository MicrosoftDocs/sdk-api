---
UID: NF:directxpackedvector.XMFLOAT3PK.XMFLOAT3PK(float,float,float)
title: XMFLOAT3PK::XMFLOAT3PK(float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMFLOAT3PK from three float arguments.
helpviewer_keywords: ["XMFLOAT3PK","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK constructor [DirectX Math Support APIs]","XMFLOAT3PK structure","XMFLOAT3PK structure [DirectX Math Support APIs]","XMFLOAT3PK constructor","XMFLOAT3PK.XMFLOAT3PK","XMFLOAT3PK.XMFLOAT3PK(float","float","float)","XMFLOAT3PK::XMFLOAT3PK","XMFLOAT3PK::XMFLOAT3PK(float","float","float)","dxmath.xmfloat3pk_ctor_2"]
old-location: dxmath\xmfloat3pk_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3PK.#ctor(float,float,float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3PK, XMFLOAT3PK constructor [DirectX Math Support APIs], XMFLOAT3PK constructor [DirectX Math Support APIs],XMFLOAT3PK structure, XMFLOAT3PK structure [DirectX Math Support APIs],XMFLOAT3PK constructor, XMFLOAT3PK.XMFLOAT3PK, XMFLOAT3PK.XMFLOAT3PK(float,float,float), XMFLOAT3PK::XMFLOAT3PK, XMFLOAT3PK::XMFLOAT3PK(float,float,float), dxmath.xmfloat3pk_ctor_2
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

# XMFLOAT3PK::XMFLOAT3PK(float,float,float)


## -description

Initializes a new instance of <code>XMFLOAT3PK</code> from three <code>float</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> from three
  <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param _x

Value to be stored in the x-component of the new instance of <code>XMFLOAT3PK</code>.
	  

The value stored is transformed from the standard 32 floating point format (sign bit,
	      8 bit exponent, 23 bit mantissa), to an 11 bit floating point format (5 bit exponent,
	      6 bit mantissa).

### -param _y

Value to be stored in the y-component of the new instance of <code>XMFLOAT3PK</code>.
	  

The value stored is transformed from the standard 32 floating point format (sign bit,
	      8 bit exponent, 23 bit mantissa), to an 11 bit floating point format (5 bit exponent,
	      6 bit mantissa).  As the target format does not support a sign bit, <b>_y</b> must be
	      greater than zero.

### -param _z

Value to be stored in the x-component of the new instance of <code>XMFLOAT3PK</code>.
	  

The value stored is transformed from the standard 32 floating point format (sign bit,
	      8 bit exponent, 23 bit mantissa), to a 10 bit floating point format (5 bit exponent,
	      5 bit mantissa).  As the target format does not support a sign bit, <b>_z</b> must be
	      greater than zero.

## -remarks

As the floating point storage formats used by <code>XMFLOAT3PK</code> do not support a sign
	   bit, all arguments to this constructor must be greater than or equal to zero.
       

Because of the change in floating point format during the instantiation of an instance of
	   <code>XMFLOAT3PK</code>, some loss of precision can be expected.

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>



<a href="/windows/desktop/dxmath/xmfloat3pk-ctor">XMFLOAT3PK Constructors</a>