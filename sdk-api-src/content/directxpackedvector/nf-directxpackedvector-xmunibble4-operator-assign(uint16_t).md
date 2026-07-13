---
UID: NF:directxpackedvector.XMUNIBBLE4.operator-assign(uint16_t)
title: XMUNIBBLE4::operator-assign(uint16_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint16_t to the current instance of XMUNIBBLE4.
helpviewer_keywords: ["XMUNIBBLE4 structure [DirectX Math Support APIs]","operator = method","XMUNIBBLE4.operator =(const uint16_t)","XMUNIBBLE4.operator-assign(uint16_t)","XMUNIBBLE4.operator=","XMUNIBBLE4::operator-assign(uint16_t)","XMUNIBBLE4::operator=","dxmath.xmunibble4_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMUNIBBLE4 structure","operator="]
old-location: dxmath\xmunibble4_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUNIBBLE4.operator = (const uint16_t)
ms.date: 12/05/2018
ms.keywords: XMUNIBBLE4 structure [DirectX Math Support APIs],operator = method, XMUNIBBLE4.operator =(const uint16_t), XMUNIBBLE4.operator-assign(uint16_t), XMUNIBBLE4.operator=, XMUNIBBLE4::operator-assign(uint16_t), XMUNIBBLE4::operator=, dxmath.xmunibble4_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMUNIBBLE4 structure, operator=
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
 - XMUNIBBLE4::operator=
 - directxpackedvector/XMUNIBBLE4::operator=
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
 - XMUNIBBLE4.operator =
---

# XMUNIBBLE4::operator-assign(uint16_t)


## -description

Assigns the vector component data packed in an instance of <code>uint16_t</code> to the current
	instance of <code>XMUNIBBLE4</code>.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of four vector components in a packed format.

## -returns

The current instance of <code>XMUNIBBLE4</code> whose vector component data has been
		updated to the component values packed in the <code>uint16_t</code> instance specified
		by the <b>Packed</b> argument.

## -remarks

The format of <b>Packed</b> is:
	

<ul>
<li>
The first 4 bits (bits 0-3) of <b>Packed</b> assigned to the <b>x</b> member of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The second 4 bits (bits 4-7) of <b>Packed</b> assigned to the
		    <b>y</b> member of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The third 4 bits (bits 8-11) of <b>Packed</b> assigned to the <b>z</b> member of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
<li>
The last 4 bits (bits 12-15) of <b>Packed</b> assigned to the <b>w</b> member of the current instance of <code>XMUNIBBLE4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>



<a href="https://msdn.microsoft.com/03b4f870-696e-4719-8115-9becb307dd10">operator = </a>

