---
UID: NF:directxpackedvector.XMU565.operator uint16_t
title: operator uint16_t function
author: windows-sdk-content
description: Returns an instance of uint16_t containing the components of the XMU555instance in a packed format.
old-location: dxmath\xmu565_operator_uint16_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU565.operator uint16_t
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DirectX::PackedVector.XMU565.operator uint16_t, DirectX::PackedVector::XMU565::operator uint16_t, XMU565 structure [DirectX Math Support APIs],operator uint16_t method, XMU565.operator uint16_t, dxmath.xmu565_operator_uint16_t, operator uint16_t method [DirectX Math Support APIs], operator uint16_t method [DirectX Math Support APIs],XMU565 structure
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
 - XMU565.operator uint16_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- operator uint16_t
: 
---

# operator uint16_t function


## -description


Returns an instance of <code>uint16_t</code> containing the components of the <code>XMU555</code>instance in a packed format.
    

This operator returns an instance of <code>uint16_t</code> containing the components of the <a href="https://msdn.microsoft.com/e3cc449d-4db8-402e-9d92-38ae5022deaf">XMU555 </a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters






## -returns



Contains the three vector components of an instance of <code>XMU555</code> in a packed
		format.
	    




## -remarks



The packed format of this operators return value is:
	

<ul>
<li>
The first 5 bits (bits 0-4) of the return value are to the <b>x</b>component of the current instance of <code>XMU555</code>.
		

</li>
<li>
The second 6 bits (bits 5-10) of the return value are to the <b>y</b>component of the current instance of <code>XMU555</code>.
		

</li>
<li>
The third 5 bits (bits 11-15) of the return value are to the <b>z</b>component of the current instance of <code>XMU555</code>.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/58c9ee71-d038-4664-9fac-5a074b60e9c3">XMU565</a>



<a href="https://msdn.microsoft.com/38869bb0-5b02-4e5c-ba66-d842a39fe417">XMU565 Operators</a>
 

 

