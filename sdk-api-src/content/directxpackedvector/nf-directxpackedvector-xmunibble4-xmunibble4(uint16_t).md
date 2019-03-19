---
UID: NF:directxpackedvector.XMUNIBBLE4.XMUNIBBLE4(uint16_t)
title: XMUNIBBLE4::XMUNIBBLE4(uint16_t) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMUNIBBLE from a uint16_t variable containing component data in a packed format.
old-location: dxmath\xmunibble4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUNIBBLE4.#ctor(uint16_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 constructor [DirectX Math Support APIs], XMUNIBBLE4 constructor [DirectX Math Support APIs],XMUNIBBLE4 structure, XMUNIBBLE4 structure [DirectX Math Support APIs],XMUNIBBLE4 constructor, XMUNIBBLE4.XMUNIBBLE4, XMUNIBBLE4.XMUNIBBLE4(uint16_t), XMUNIBBLE4::XMUNIBBLE4, XMUNIBBLE4::XMUNIBBLE4(uint16_t), dxmath.xmunibble4_ctor_2
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
 - XMUNIBBLE4.XMUNIBBLE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMUNIBBLE4::XMUNIBBLE4(uint16_t)


## -description


Initializes a new instance of <code>XMUNIBBLE</code> from a <code>uint16_t</code> variable
	  containing component data in a packed format.
  

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee420614(v=VS.85).aspx">XMUNIBBLE4</a> from a
	  <code>uint16_t</code> variable containing component data in a packed format.
  
<div class="alert"><b>Note</b>  This constructor is only available under C++.
  </div><div> </div>

## -parameters




### -param Packed

The values of four vector components in a packed format.
	    


## -remarks



The values defining the four components of the new instance of <code>XMUNIBBLE4</code> are
	    stored in the argument <code>Packed</code> as follows:
	  

<ul>
<li>
The first 4 bits (bits 0-3) of <b>Packed</b> assigned, as an integer, to the
		      <b>x</b> member of the instance of <code>XMUNIBBLE4</code> constructed.
		    

</li>
<li>
The second 4 bits (bits 4-7) of <b>Packed</b> assigned, as an integer, to
		      the <b>y</b> member of the instance of <code>XMUNIBBLE4</code> constructed.
		    

</li>
<li>
The third 4 bits (bits 8-11) of <b>Packed</b> assigned, as an integer, to
		      the <b>z</b> member of the instance of <code>XMUNIBBLE4</code> constructed.
		    

</li>
<li>
The last 4 bits (bits 12-15) of <b>Packed</b> assigned, as an integer, to
		      the <b>w</b> member of the instance of <code>XMUNIBBLE4</code> constructed.
		    

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee420614(v=VS.85).aspx">XMUNIBBLE4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415488(v=VS.85).aspx">XMUNIBBLE4 Constructors</a>
 

 

