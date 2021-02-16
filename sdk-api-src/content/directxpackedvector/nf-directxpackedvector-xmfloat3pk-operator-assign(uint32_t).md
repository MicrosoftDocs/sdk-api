---
UID: NF:directxpackedvector.XMFLOAT3PK.operator-assign(uint32_t)
title: XMFLOAT3PK::operator-assign(uint32_t) (directxpackedvector.h)
description: This operator assigns the vector component data packed in an instance of uint32_t to the current instance of XMFLOAT3PK.
helpviewer_keywords: ["XMFLOAT3PK structure [DirectX Math Support APIs]","operator = method","XMFLOAT3PK.operator =(const uint32_t)","XMFLOAT3PK.operator-assign(uint32_t)","XMFLOAT3PK.operator=","XMFLOAT3PK::operator-assign(uint32_t)","XMFLOAT3PK::operator=","dxmath.xmfloat3pk_operator_eq_2","operator = method [DirectX Math Support APIs]","operator = method [DirectX Math Support APIs]","XMFLOAT3PK structure","operator="]
old-location: dxmath\xmfloat3pk_operator_eq_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3PK.operator = (const uint32_t)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3PK structure [DirectX Math Support APIs],operator = method, XMFLOAT3PK.operator =(const uint32_t), XMFLOAT3PK.operator-assign(uint32_t), XMFLOAT3PK.operator=, XMFLOAT3PK::operator-assign(uint32_t), XMFLOAT3PK::operator=, dxmath.xmfloat3pk_operator_eq_2, operator = method [DirectX Math Support APIs], operator = method [DirectX Math Support APIs],XMFLOAT3PK structure, operator=
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
 - XMFLOAT3PK::operator=
 - directxpackedvector/XMFLOAT3PK::operator=
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
 - XMFLOAT3PK.operator =
---

# XMFLOAT3PK::operator-assign(uint32_t)


## -description

This operator assigns the vector component data packed in an instance of <code>uint32_t</code> to
     the current instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>.
 
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of three vector components in a packed format.

## -returns

The current instance of <code>XMFLOAT3PK</code> whose vector component data has been updated to
	  the component values packed in the <code>uint32_t</code> instance specified by the
	  <b>Packed</b> argument.

## -remarks

The values of the three components assigned to the current instance of <code>XMFLOAT3PK</code> are stored
	in the argument <b>Packed</b> with the z component (as a reduced precision
	floating point number) in the most significant bits, and the x component is stored in the
	least significant bits:
 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
  (Z10Y11X11): [32] ZZZZZzzz zzYYYYYy yyyyyXXX XXxxxxxx [0]
</pre>
</td>
</tr>
</table></span></div>
Or in detail:


<ul>
<li>
Bits 0-5 of <b>v</b> are the 6 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value: the <b>xm</b> member of the current structure.
	    

</li>
<li>
Bits 6-10 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>x</b> component's floating point value the <b>xe</b> member of the current structure.
	    

</li>
<li>
Bits 11-16 of <b>v</b> are the 6-bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value: the <b>ym</b> member of the current structure.
	    

</li>
<li>
Bits 17-21 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>y</b> component's floating point value: the <b>ye</b> member of the current structure.
	    

</li>
<li>
Bits 22-26 of <b>v</b> are the 5 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value: the <b>zm</b> member of the current structure.
	    

</li>
<li>
Bits 27-31 of <b>v</b> are the 5 bit <i>exponent</i> of the
		<b>z</b> component's floating point value: the <b>ze</b> member of the current structure.
	    

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk">XMFLOAT3PK</a>



<a href="https://msdn.microsoft.com/82c6ee72-0706-49f9-bc19-9725496440d0">operator = </a>

