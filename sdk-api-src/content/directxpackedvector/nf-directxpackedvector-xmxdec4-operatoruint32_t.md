---
UID: NF:directxpackedvector.XMXDEC4.operator-cast-uint32_t
title: XMXDEC4::operator uint32_t (directxpackedvector.h)
description: Returns an instance of uint32_t containing the components of the XMXDEC4instance in a packed format.
helpviewer_keywords: ["DirectX::PackedVector.XMXDEC4.operator uint32_t","DirectX::PackedVector::XMXDEC4::operator uint32_t","XMXDEC4 structure [DirectX Math Support APIs]","operator uint32_t method","XMXDEC4.operator uint32_t","XMXDEC4::operator uint32_t","dxmath.xmxdec4_operator_uint32_t","operator uint32_t","operator uint32_t method [DirectX Math Support APIs]","operator uint32_t method [DirectX Math Support APIs]","XMXDEC4 structure"]
old-location: dxmath\xmxdec4_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDEC4.operator uint32_t
ms.date: 12/05/2018
ms.keywords: DirectX::PackedVector.XMXDEC4.operator uint32_t, DirectX::PackedVector::XMXDEC4::operator uint32_t, XMXDEC4 structure [DirectX Math Support APIs],operator uint32_t method, XMXDEC4.operator uint32_t, XMXDEC4::operator uint32_t, dxmath.xmxdec4_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMXDEC4 structure
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
 - XMXDEC4::operator uint32_t
 - directxpackedvector/XMXDEC4::operator uint32_t
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
 - XMXDEC4.operator uint32_t
---

# XMXDEC4::operator uint32_t


## -description

Returns an instance of <code>uint32_t</code> containing the components of the <code>XMXDEC4</code> instance in a packed format.
    

This operator returns an instance of <code>uint32_t</code> containing the components of the <a href="https://msdn.microsoft.com/5b46e0fb-e4a5-49c4-8084-0c631d43d4f7">XMXDEC4
	</a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>



## -returns

Contains the four vector components of an instance of <code>XMXDEC4</code> in a packed
		format.

## -remarks

The packed format of this operators return value is:
	

<ul>
<li>
The first 20 bits (bits 0-09) of the return value are to the <b>x</b> component of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The second 20 bits (bits 10-19) of the return value are to the <b>y</b> component of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The third 20 bits (bits 20-29) of the return value are to the <b>z</b> component of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The last 4 bits (bits 30-31) of the return value are to the <b>w</b> component of the current instance of <code>XMXDEC4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4</a>



<a href="/windows/desktop/dxmath/ovw-xmxdec4-operators">XMXDEC4 Operators</a>
