---
UID: NF:directxpackedvector.XMFLOAT3SE.operator uint32_t
title: XMFLOAT3SE::operator uint32_t
author: windows-sdk-content
description: Returns an instance of uint32_t containing the components of the XMFLOAT3SE instance in a packed format.
old-location: dxmath\xmfloat3se_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3SE.operator uint32_t
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DirectX::PackedVector.XMFLOAT3SE.operator uint32_t, DirectX::PackedVector::XMFLOAT3SE::operator uint32_t, XMFLOAT3SE structure [DirectX Math Support APIs],operator uint32_t method, XMFLOAT3SE.operator uint32_t, XMFLOAT3SE::operator uint32_t, dxmath.xmfloat3se_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMFLOAT3SE structure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMFLOAT3SE.operator uint32_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMFLOAT3SE::operator uint32_t


## -description


Returns an instance of <code>uint32_t</code> containing the components of the
<code>XMFLOAT3SE</code> instance in a packed format.

This operator returns an instance of <code>uint32_t</code> containing the components of the
    <a href="https://msdn.microsoft.com/en-us/library/Ee419489(v=VS.85).aspx">XMFLOAT3SE</a> instance in a packed format.

<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters






## -returns



Contains the three vector components of an instance of  <code>XMFLOAT3SE</code> in a packed format.
      




## -remarks



The values of the three components of the current instance of <code>XMFLOAT3SE</code> are
	returned in the following format: the <b>e</b> member of the <code>XMFLOAT3SE</code>structure -- the exponent shared by the mantissas of the floating point values of all
	three components of <code>XMFLOAT3SE</code> -- is stored in the highest order bits of the
	return value, and the mantissa of the x component stored in the least significant bits.
 

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
Bits 0-8 of the return value are the 9 bit <i>mantissa</i> of the
	       <b>x</b> component's floating point value: the <b>xm</b> member of the current structure.
	    

</li>
<li>
Bits 9-17 of the return value are the 9 bit <i>mantissa</i> of the
	       <b>y</b> component's floating point value: the <b>ym</b> member of the current structure.
	    

</li>
<li>
Bits 18-26 of the return value are the 9 bit <i>mantissa</i> of the
	       <b>z</b> component's floating point value: the <b>zm</b> member of the current structure.
	    

</li>
<li>
Bits 27-31 of the return value are the 5 bit <i>exponent</i> used
		with the stored mantissas (<b>xm</b>, <b>ym</b>,
		<b>zm</b>) to represent the size of each component: the <b>e</b> member of the current structure.
	    

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419489(v=VS.85).aspx">XMFLOAT3SE</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415287(v=VS.85).aspx">XMFLOAT3SE Operators</a>
 

 

