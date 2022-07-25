---
UID: NF:directxpackedvector.XMXDEC4.operator-assign(uint32_t)
title: XMXDEC4::operator-assign(uint32_t) (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint32_t to the current instance of XMXDEC4.
helpviewer_keywords: ["XMXDEC4 structure [DirectX Math Support APIs]","operator = method","XMXDEC4.operator =(const uint32_t)","XMXDEC4.operator-assign(uint32_t)","XMXDEC4.operator=","XMXDEC4::operator-assign(uint32_t)","XMXDEC4::operator=","dxmath.xmxdec4_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMXDEC4 structure","operator="]
old-location: dxmath\xmxdec4_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDEC4.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMXDEC4 structure [DirectX Math Support APIs],operator = method, XMXDEC4.operator =(const uint32_t), XMXDEC4.operator-assign(uint32_t), XMXDEC4.operator=, XMXDEC4::operator-assign(uint32_t), XMXDEC4::operator=, dxmath.xmxdec4_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMXDEC4 structure, operator=
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
 - XMXDEC4::operator=
 - directxpackedvector/XMXDEC4::operator=
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
 - XMXDEC4.operator =
---

# XMXDEC4::operator-assign(uint32_t)


## -description

Assigns the vector component data packed in an instance of <code>uint32_t</code> to the current
	instance of <code>XMXDEC4</code>.
    

This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to
	the current instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of four vector components in a packed format.

## -returns

The current instance of <code>XMXDEC4</code> whose vector component data has been
		updated to the component values packed in the <code>uint32_t</code> instance specified by
		the <b>Packed</b> argument.

## -remarks

The format of <b>Packed</b> is:
	

<ul>
<li>
The first 10 bits (bits 0-09) of <b>Packed</b> assigned to the <b>x</b> member of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned to the <b>y</b> member of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The third 10 bits (bits 10-29) of <b>Packed</b> assigned to the <b>z</b> member of the current instance of <code>XMXDEC4</code>.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned to the <b>w</b> member of the current instance of <code>XMXDEC4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4</a>



<a href="https://msdn.microsoft.com/07952c7d-0d87-4c93-9a91-d72c702c6200">operator = </a>

