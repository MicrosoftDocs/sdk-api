---
UID: NF:directxpackedvector.XMXDECN4.operator-assign(uint32_t)
title: XMXDECN4::operator-assign(uint32_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint32_t to the current instance of XMXDECN4.
helpviewer_keywords: ["XMXDECN4 structure [DirectX Math Support APIs]","operator = method","XMXDECN4.operator =(const uint32_t)","XMXDECN4.operator-assign(uint32_t)","XMXDECN4.operator=","XMXDECN4::operator-assign(uint32_t)","XMXDECN4::operator=","dxmath.xmxdecn4_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMXDECN4 structure","operator="]
old-location: dxmath\xmxdecn4_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDECN4.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMXDECN4 structure [DirectX Math Support APIs],operator = method, XMXDECN4.operator =(const uint32_t), XMXDECN4.operator-assign(uint32_t), XMXDECN4.operator=, XMXDECN4::operator-assign(uint32_t), XMXDECN4::operator=, dxmath.xmxdecn4_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMXDECN4 structure, operator=
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
 - XMXDECN4::operator=
 - directxpackedvector/XMXDECN4::operator=
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
 - XMXDECN4.operator =
---

# XMXDECN4::operator-assign(uint32_t)


## -description

Assigns the vector component data packed in an instance of <code>uint32_t</code> to the current
	instance of <code>XMXDECN4</code>.
    

This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to
	the current instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of four vector components in a packed format.

## -returns

The current instance of <code>XMXDECN4</code> whose vector component data has been
		updated to the component values packed in the <code>uint32_t</code> instance specified by
		the <b>Packed</b> argument.

## -remarks

The format of <b>Packed</b> is:
	

<ul>
<li>
The first 120 bits (bits 0-9) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>x</b> member of the current instance of
		    <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>y</b> member of the current instance of
		    <code>XMXDECN4</code>.
		

</li>
<li>
The third 10 bits (bits 20-29) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>z</b> member of the current instance of
		    <code>XMXDECN4</code>.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>w</b> member of the current instance of
		    <code>XMXDECN4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdecn4">XMXDECN4</a>



<a href="https://msdn.microsoft.com/d60f196b-281a-428c-bdae-f2d4ad1e206d">operator = </a>