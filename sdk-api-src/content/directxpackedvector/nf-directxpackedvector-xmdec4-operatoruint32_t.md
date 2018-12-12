---
UID: NF:directxpackedvector.XMDEC4.operator uint32_t
title: XMDEC4::operator uint32_t
author: windows-sdk-content
description: Returns an instance of uint32_t containing the components of the XMDEC4instance in a packed format.
old-location: dxmath\xmdec4_operator_uint32_t.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMDEC4.operator uint32_t
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DirectX::PackedVector.XMDEC4.operator uint32_t, DirectX::PackedVector::XMDEC4::operator uint32_t, XMDEC4 structure [DirectX Math Support APIs],operator uint32_t method, XMDEC4.operator uint32_t, XMDEC4::operator uint32_t, dxmath.xmdec4_operator_uint32_t, operator uint32_t, operator uint32_t method [DirectX Math Support APIs], operator uint32_t method [DirectX Math Support APIs],XMDEC4 structure
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
 - XMDEC4.operator uint32_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMDEC4::operator uint32_t


## -description


Returns an instance of <code>uint32_t</code> containing the components of the <code>XMDEC4</code>instance in a packed format.
    

This operator returns an instance of <code>uint32_t</code> containing the components of the <a href="https://msdn.microsoft.com/a52fa5e4-ee45-4256-a06a-6984d63b5578">XMDEC4 
	</a> instance in a packed format.
<div class="alert"><b>Note</b>  This operator is only available under C++.
    </div><div> </div>

## -parameters






## -returns



Contains the four vector components of an instance of <code>XMDEC4</code> in a packed
		format.
	    




## -remarks



The packed format of this operators return value is:
	

<ul>
<li>
The first 20 bits (bits 0-09) of the return value are to the <b>x</b>component of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The second 20 bits (bits 10-19) of the return value are to the <b>y</b>component of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The third 20 bits (bits 20-29) of the return value are to the <b>z</b>component of the current instance of <code>XMDEC4</code>.
		

</li>
<li>
The last 4 bits (bits 30-31) of the return value are to the <b>w</b>component of the current instance of <code>XMDEC4</code>.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419431(v=VS.85).aspx">XMDEC4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415269(v=VS.85).aspx">XMDEC4 Operators</a>
 

 

