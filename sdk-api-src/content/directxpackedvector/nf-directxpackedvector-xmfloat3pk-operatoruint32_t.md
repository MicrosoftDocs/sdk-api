---
UID: NF:directxpackedvector.XMFLOAT3PK.operator-cast-uint32_t
title: XMFLOAT3PK::operator uint32_t (directxpackedvector.h)
description: Returns an instance of uint32_t containing the components of the XMFLOAT3PK instance in a packed format.
helpviewer_keywords: ["DirectX::PackedVector.XMFLOAT3PK.operator uint32_t","DirectX::PackedVector::XMFLOAT3PK::operator uint32_t","XMFLOAT3PK structure [DirectX Math Support APIs]","operator uint32_t method","XMFLOAT3PK.operator uint32_t","XMFLOAT3PK::operator uint32_t","dxmath.xmfloat3pk_operator_uint32_t","operator uint32_t","operator uint32_t method [DirectX Math Support APIs]","operator uint32_t method [DirectX Math Support APIs]","XMFLOAT3PK structure"]
old-location: dxmath\xmfloat3pk_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3PK.operator uint32_t
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMFLOAT3PK.operator uint32_t, DirectX::PackedVector::XMFLOAT3PK::operator uint32_t, XMFLOAT3PK structure [DirectX Math Support APIs],operator uint32_t method, XMFLOAT3PK.operator uint32_t, XMFLOAT3PK::operator uint32_t, dxmath.xmfloat3pk_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMFLOAT3PK structure
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
 - XMFLOAT3PK::operator uint32_t
 - directxpackedvector/XMFLOAT3PK::operator uint32_t
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
 - XMFLOAT3PK.operator uint32_t
---

# XMFLOAT3PK::operator uint32_t


## -description

Returns an instance of <code>uint32_t</code> containing the components of the
<code>XMFLOAT3PK</code> instance in a packed format.

This operator returns an instance of <code>uint32_t</code> containing the components of the
    <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a> instance in a packed format.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>



## -returns

Contains the three vector components of an instance of
	  <code>XMFLOAT3PK</code> in a packed format.

## -remarks

The values of the three components of the current instance of <code>XMFLOAT3PK</code> are
	returned packed in a <code>uint32_t</code> with the z component (as a reduced precision floating
	point number) in the most significant bits, and the x component is stored in the least
	significant bits:
 


```

  (Z10Y11X11): [32] ZZZZZzzz zzYYYYYY yyyyyXXX XXXxxxxx [0]

```


Or in detail:


<ul>
<li>
Bits 0-5 of the return value are the 6 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value.
	    

</li>
<li>
Bits 6-10 of the return value are the 5 bit <i>exponent</i> of the
		<b>x</b> component's floating point value.
	    

</li>
<li>
Bits 11-16 of the return value are the 6-bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value.
	    

</li>
<li>
Bits 17-21 of the return value are the 5 bit <i>exponent</i> of the
		<b>y</b> component's floating point value.
	    

</li>
<li>
Bits 22-26 of the return value are the 5 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value.
	    

</li>
<li>
Bits 27-31 of the return value are the 5 bit <i>exponent</i> of the
		<b>z</b> component's floating point value.
	    

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>



<a href="/windows/desktop/dxmath/ovw-xmfloat3pk-operators">XMFLOAT3PK Operators</a>
