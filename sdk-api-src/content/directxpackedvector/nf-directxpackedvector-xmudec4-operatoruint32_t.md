---
UID: NF:directxpackedvector.XMUDEC4.operator uint32_t
title: XMUDEC4::operator uint32_t
author: windows-sdk-content
description: Returns an instance of uint32_t containing the components of the XMUDEC4instance in a packed format.
old-location: dxmath\xmudec4_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUDEC4.operator uint32_t
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DirectX::PackedVector.XMUDEC4.operator uint32_t, DirectX::PackedVector::XMUDEC4::operator uint32_t, XMUDEC4 structure [DirectX Math Support APIs],operator uint32_t method, XMUDEC4.operator uint32_t, XMUDEC4::operator uint32_t, dxmath.xmudec4_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMUDEC4 structure
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
 - XMUDEC4.operator uint32_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUDEC4::operator uint32_t


## -description


Returns an instance of <code>uint32_t</code> containing the components of the <code>XMUDEC4</code>instance in a packed format.
    

This operator returns an instance of <code>uint32_t</code> containing the components of the <a href="https://msdn.microsoft.com/CD99837B-7031-4609-B19F-785DD26773D0">XMUDEC4 
	</a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters






## -returns



Contains the four vector components of an instance of <code>XMUDEC4</code> in a packed
		format.
	    




## -remarks



The packed format of this operators return value is:
	

<ul>
<li>
The first 20 bits (bits 0-09) of the return value are to the <b>x</b>component of the current instance of <code>XMUDEC4</code>.
		

</li>
<li>
The second 20 bits (bits 10-19) of the return value are to the <b>y</b>component of the current instance of <code>XMUDEC4</code>.
		

</li>
<li>
The third 20 bits (bits 20-29) of the return value are to the <b>z</b>component of the current instance of <code>XMUDEC4</code>.
		

</li>
<li>
The last 4 bits (bits 30-31) of the return value are to the <b>w</b>component of the current instance of <code>XMUDEC4</code>.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/CD99837B-7031-4609-B19F-785DD26773D0">XMUDEC4</a>



<a href="https://msdn.microsoft.com/d199a583-cbff-4421-a330-ac4caf43d87d">XMUDEC4 Operators</a>
 

 

