---
UID: NF:directxpackedvector.XMXDECN4.operator-cast-uint32_t
title: XMXDECN4::operator uint32_t (directxpackedvector.h)
description: Returns an instance of uint32_t containing the components of the XMXDECN4instance in a packed format.
helpviewer_keywords: ["DirectX::PackedVector.XMXDECN4.operator uint32_t","DirectX::PackedVector::XMXDECN4::operator uint32_t","XMXDECN4 structure [DirectX Math Support APIs]","operator uint32_t method","XMXDECN4.operator uint32_t","XMXDECN4::operator uint32_t","dxmath.xmxdecn4_operator_uint32_t","operator uint32_t","operator uint32_t method [DirectX Math Support APIs]","operator uint32_t method [DirectX Math Support APIs]","XMXDECN4 structure"]
old-location: dxmath\xmxdecn4_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDECN4.operator uint32_t
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMXDECN4.operator uint32_t, DirectX::PackedVector::XMXDECN4::operator uint32_t, XMXDECN4 structure [DirectX Math Support APIs],operator uint32_t method, XMXDECN4.operator uint32_t, XMXDECN4::operator uint32_t, dxmath.xmxdecn4_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMXDECN4 structure
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
 - XMXDECN4::operator uint32_t
 - directxpackedvector/XMXDECN4::operator uint32_t
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
 - XMXDECN4.operator uint32_t
---

# XMXDECN4::operator uint32_t


## -description

Returns an instance of <code>uint32_t</code> containing the components of the <code>XMXDECN4</code> instance in a packed format.
    

Returns an instance of <code>uint32_t</code> containing the components of the <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>



## -returns

Contains the four vector components of an instance of <code>XMXDECN4</code> in a packed
		format.

## -remarks

The values of the <code>XMXDECN4</code> components returned are not normalized, and are in
	    the following format:
	    
	

<ul>
<li>
The first 10 bits (bits 0- 9) of the return value are the <b>x</b> component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The second 10 bits (bits 10-19) of the return value are the <b>y</b> component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The third 10 bits (bits 20-29) of the return value are the <b>z</b> component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The last 2 bits (bits 30-31) of the return value are the <b>w</b> component
		    of the current instance of <code>XMXDECN4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a>



<a href="/windows/desktop/dxmath/ovw-xmxdecn4-operators">XMXDECN4 Operators</a>
