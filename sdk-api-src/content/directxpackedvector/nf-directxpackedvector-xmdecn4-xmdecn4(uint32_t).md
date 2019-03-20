---
UID: NF:directxpackedvector.XMDECN4.XMDECN4(uint32_t)
title: XMDECN4::XMDECN4(uint32_t) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMDECN4 from a uint32_t variable containing component data in a packed format.
old-location: dxmath\xmdecn4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMDECN4.#ctor(uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMDECN4, XMDECN4 constructor [DirectX Math Support APIs], XMDECN4 constructor [DirectX Math Support APIs],XMDECN4 structure, XMDECN4 structure [DirectX Math Support APIs],XMDECN4 constructor, XMDECN4.XMDECN4, XMDECN4.XMDECN4(uint32_t), XMDECN4::XMDECN4, XMDECN4::XMDECN4(uint32_t), dxmath.xmdecn4_ctor_2
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
 - XMDECN4.XMDECN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMDECN4::XMDECN4(uint32_t)


## -description


Initializes a new instance of <code>XMDECN4</code> from a <code>uint32_t</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419440(v=VS.85).aspx">XMDECN4 </a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param Packed

The values of four vector components in a packed format.
		    
		


## -remarks



The values defining the four components of the new instance of <code>XMDECN4</code> are
	    not normalized and are stored in the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 10 bits (bits 0-9) of <b>Packed</b> assigned, as an integer, to
		    the <b>x</b> member of the instance of <code>XMDECN4</code> constructed.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned, as an integer, to
		    the <b>y</b> member of the instance of <code>XMDECN4</code> constructed.
		

</li>
<li>
The third 10 bits (bits 20-29) of <b>Packed</b> assigned, as an integer, to
		    the <b>z</b> member of the instance of <code>XMDECN4</code> constructed.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned, as an integer, to
		    the <b>w</b> member of the instance of <code>XMDECN4</code> constructed.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419440(v=VS.85).aspx">XMDECN4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415270(v=VS.85).aspx">XMDECN4 Constructors</a>
 

 

