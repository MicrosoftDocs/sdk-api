---
UID: NF:directxpackedvector.XMDEC4.operator-cast-uint32_t
title: XMDEC4::operator uint32_t (directxpackedvector.h)
description: Assigns the vector component data packed in an instance of uint32_t to the current instance of XMDEC4.
helpviewer_keywords: ["XMDEC4 structure [DirectX Math Support APIs]","operator = method","XMDEC4.operator =(const uint32_t)","XMDEC4.operator uint32_t","XMDEC4::operator uint32_t","dxmath.xmdec4_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMDEC4 structure","operator uint32_t"]
old-location: dxmath\xmdec4_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMDEC4.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMDEC4 structure [DirectX Math Support APIs],operator = method, XMDEC4.operator =(const uint32_t), XMDEC4.operator uint32_t, XMDEC4::operator uint32_t, dxmath.xmdec4_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMDEC4 structure, operator uint32_t
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
 - XMDEC4::operator uint32_t
 - directxpackedvector/XMDEC4::operator uint32_t
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
 - XMDEC4.operator =
---

## -description

Assigns the vector component data packed in an instance of <code>uint32_t</code> to the current
	instance of <code>XMDEC4</code>.
    
This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to
	the current instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmdec4">XMDEC4</a>.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>



## -returns

The current instance of <code>XMDEC4</code> whose vector component data has been
		updated to the component values packed in the <code>uint32_t</code> instance specified by
		the <b>Packed</b> argument.

## -remarks

The format of <b>Packed</b> is:
	

<ul>
<li>
The first 10 bits (bits 0-09) of <b>Packed</b> assigned to the <b>x</b> member of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned to the <b>y</b> member of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The third 10 bits (bits 10-29) of <b>Packed</b> assigned to the <b>z</b> member of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned to the <b>w</b> member of the current instance of <code>XMDEC4</code>.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmdec4">XMDEC4</a>



<a href="https://msdn.microsoft.com/46a34196-d32a-4ddf-9245-c568b9461f7d">operator = </a>
