---
UID: NF:directxpackedvector.XMXDECN4.operator uint32_t
title: operator uint32_t function
author: windows-sdk-content
description: Returns an instance of uint32_t containing the components of the XMXDECN4instance in a packed format.
old-location: dxmath\xmxdecn4_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDECN4.operator uint32_t
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DirectX::PackedVector.XMXDECN4.operator uint32_t, DirectX::PackedVector::XMXDECN4::operator uint32_t, XMXDECN4 structure [DirectX Math Support APIs],operator uint32_t method, XMXDECN4.operator uint32_t, dxmath.xmxdecn4_operator_uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMXDECN4 structure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - XMXDECN4.operator uint32_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- operator uint32_t
: 
---

# operator uint32_t function


## -description


Returns an instance of <code>uint32_t</code> containing the components of the <code>XMXDECN4</code>instance in a packed format.
    

Returns an instance of <code>uint32_t</code> containing the components of the <a href="https://msdn.microsoft.com/705A1848-26BC-47E5-9209-C0DF843DE6AE">XMXDECN4</a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.</div><div> </div>

## -parameters






## -returns



Contains the four vector components of an instance of <code>XMXDECN4</code> in a packed
		format.
	    




## -remarks



The values of the <code>XMXDECN4</code> components returned are not normalized, and are in
	    the following format:
	    
	

<ul>
<li>
The first 10 bits (bits 0- 9) of the return value are the <b>x</b>component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The second 10 bits (bits 10-19) of the return value are the <b>y</b>component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The third 10 bits (bits 20-29) of the return value are the <b>z</b>component of the current instance of <code>XMXDECN4</code>.
		

</li>
<li>
The last 2 bits (bits 30-31) of the return value are the <b>w</b> component
		    of the current instance of <code>XMXDECN4</code>.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/705A1848-26BC-47E5-9209-C0DF843DE6AE">XMXDECN4</a>



<a href="https://msdn.microsoft.com/23e966a6-eca1-450d-98c4-3b4e5c6706ab">XMXDECN4 Operators</a>
 

 

