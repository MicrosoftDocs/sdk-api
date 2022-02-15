---
UID: NF:directxpackedvector.XMUNIBBLE4.operator-cast-uint16_t
title: XMUNIBBLE4::operator uint16_t (directxpackedvector.h)
description: Returns an instance of uint16_t containing the components of the XMUNIBBLE4 instance in a packed format.
helpviewer_keywords: ["DirectX::PackedVector.XMUNIBBLE4.operator uint16_t","DirectX::PackedVector::XMUNIBBLE4::operator uint16_t","XMUNIBBLE4 structure [DirectX Math Support APIs]","operator uint16_t method","XMUNIBBLE4.operator uint16_t","XMUNIBBLE4::operator uint16_t","dxmath.xmunibble4_operator_uint16_t","operator uint16_t","operator uint16_t method [DirectX Math Support APIs]","operator uint16_t method [DirectX Math Support APIs]","XMUNIBBLE4 structure"]
old-location: dxmath\xmunibble4_operator_uint16_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUNIBBLE4.operator uint16_t
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMUNIBBLE4.operator uint16_t, DirectX::PackedVector::XMUNIBBLE4::operator uint16_t, XMUNIBBLE4 structure [DirectX Math Support APIs],operator uint16_t method, XMUNIBBLE4.operator uint16_t, XMUNIBBLE4::operator uint16_t, dxmath.xmunibble4_operator_uint16_t, operator uint16_t, operator uint16_t method [DirectX Math Support APIs], operator uint16_t method [DirectX Math Support APIs],XMUNIBBLE4 structure
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
 - XMUNIBBLE4::operator uint16_t
 - directxpackedvector/XMUNIBBLE4::operator uint16_t
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
 - XMUNIBBLE4.operator uint16_t
---

# XMUNIBBLE4::operator uint16_t


## -description

Returns an instance of <code>uint16_t</code> containing the components of the
	<code>XMUNIBBLE4</code> instance in a packed format.
    

This operator returns an instance of <code>uint16_t</code> containing the components of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4 </a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>



## -returns

Contains the four vector components of an instance of <code>XMUNIBBLE4</code> in a packed
		format.

## -remarks

The packed format of this operators return value is:
	

<ul>
<li>
The first 4 bits (bits 0-3) of the return value are to the <b>x</b> component of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The second 4 bits (bits 4-7) of the return value are to the <b>y</b> component of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The third 4 bits (bits 8-11) of the return value are to the <b>z</b> component of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The last 4 bits (bits 12-15) of the return value are to the <b>w</b> component of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>



<a href="/windows/desktop/dxmath/ovw-xmunibble4-operators">XMUNIBBLE4 Operators</a>
