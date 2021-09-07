---
UID: NF:directxpackedvector.XMFLOAT3SE.operator-assign(uint32_t)
title: XMFLOAT3SE::operator-assign(uint32_t) (directxpackedvector.h)
description: This operator assigns the vector component data packed in an instance of uint32_t to the current instance of XMFLOAT3SE.
helpviewer_keywords: ["XMFLOAT3SE structure [DirectX Math Support APIs]","operator = method","XMFLOAT3SE.operator =(const uint32_t)","XMFLOAT3SE.operator-assign(uint32_t)","XMFLOAT3SE.operator=","XMFLOAT3SE::operator-assign(uint32_t)","XMFLOAT3SE::operator=","dxmath.xmfloat3se_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMFLOAT3SE structure","operator="]
old-location: dxmath\xmfloat3se_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3SE.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3SE structure [DirectX Math Support APIs],operator = method, XMFLOAT3SE.operator =(const uint32_t), XMFLOAT3SE.operator-assign(uint32_t), XMFLOAT3SE.operator=, XMFLOAT3SE::operator-assign(uint32_t), XMFLOAT3SE::operator=, dxmath.xmfloat3se_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMFLOAT3SE structure, operator=
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
 - XMFLOAT3SE::operator=
 - directxpackedvector/XMFLOAT3SE::operator=
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
 - XMFLOAT3SE.operator =
---

# XMFLOAT3SE::operator-assign(uint32_t)


## -description

This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to
     the current instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a>.
 
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of three vector components in a packed format.

## -returns

The current instance of <code>XMFLOAT3SE</code> whose vector component data has been updated to
	  the component values packed in the <code>uint32_t</code> instance specified by the
	  <b>Packed</b> argument.

## -remarks

The values of the three components of the updated current instance of <code>XMFLOAT3SE</code> are loaded from the argument <b>Packed</b>. The format of these data have the
	<b>e</b> member of the <code>XMFLOAT3SE</code> structure -- the exponent shared by the
	mantissas of the floating point values of all three stored components -- is stored in the highest order
	bits of <b>Packed</b>, and the mantissa of the x component stored in the least significant bits.
 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
   (E5Z9Y9X9): [32] EEEEEzzz zzzzzzyy yyyyyyyx xxxxxxxx [0]
</pre>
</td>
</tr>
</table></span></div>
Or in detail:


<ul>
<li>
Bits 0-8 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value: the <b>xm</b> member of the current structure.
	    

</li>
<li>
Bits 9-17 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value: the <b>ym</b> member of the current structure.
	    

</li>
<li>
Bits 18-26 of <b>Packed</b> are the 9 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value: the <b>zm</b> member of the current structure.
	    

</li>
<li>
Bits 27-31 of <b>Packed</b> are the 5 bit <i>exponent</i> used
		with the stored mantissas (<b>xm</b>, <b>ym</b>,
		<b>zm</b>) to represent the size of each component: the <b>e</b> member of the current structure.
	    

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se">XMFLOAT3SE</a>



<a href="https://msdn.microsoft.com/e3c74a38-65ab-48ac-931d-1fc66ec04d74">operator = </a>

