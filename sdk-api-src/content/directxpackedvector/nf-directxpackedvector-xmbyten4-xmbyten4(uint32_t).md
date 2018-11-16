---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(uint32_t)
title: XMBYTEN4 function
author: windows-sdk-content
description: Initializes a new instance of XMBYTEN4 from a uint32_tvariable containing component data in a packed format.
old-location: dxmath\xmbyten4_ctor_6.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN4.#ctor(uint32_t)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4(uint32_t), dxmath.xmbyten4_ctor_6
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
 - XMBYTEN4.XMBYTEN4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMBYTEN4
: 
---

# XMBYTEN4 function


## -description


Initializes a new instance of <code>XMBYTEN4</code> from a <code>uint32_t</code>variable containing component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/62d61a35-8674-4855-b09c-f351363cd50b">XMBYTEN4 
	</a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param Packed

The values of four vector components of the new instance, in a packed format.
	    


## -remarks



The values defining the three components of the new instance of <code>XMBYTEN4</code> are
	    not normalized, and are stored in the argument <code>Packed</code> in the following
	    format:
	

<ul>
<li>
The first 8 bits (bits 0-7) of <b>Packed</b> assigned, as an signed
		    integer, to the <b>x</b> member of the instance of <code>XMBYTEN4</code>constructed.
		

</li>
<li>
The second 8 bits (bits 8-15) of <b>Packed</b> assigned, as an signed
		    integer, to the <b>y</b> member of the instance of <code>XMBYTEN4</code>constructed.
		

</li>
<li>
The third 8 bits (bits 16-23) of <b>Packed</b> assigned, as an signed
		    integer, to the <b>z</b> member of the instance of <code>XMBYTEN4</code>constructed.
		

</li>
<li>
The last 8 bits (bits 24-31) of <b>Packed</b> assigned, as an signed
		    integer, to the <b>w</b> member of the instance of <code>XMBYTEN4</code>constructed.
		

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/62d61a35-8674-4855-b09c-f351363cd50b">XMBYTEN4</a>



<a href="https://msdn.microsoft.com/f90dfcdc-689c-4d0e-9c11-06d29b134901">XMBYTEN4 Constructors</a>
 

 

