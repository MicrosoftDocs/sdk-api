---
UID: NF:directxpackedvector.XMBYTE4.XMBYTE4(uint32_t)
title: XMBYTE4::XMBYTE4(uint32_t) (directxpackedvector.h)
author: windows-sdk-content
description: Initializes a new instance of XMBYTE4 from a uint32_tvariable containing component data in a packed format.
old-location: dxmath\xmbyte4_ctor_6.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTE4.#ctor(uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMBYTE4, XMBYTE4 constructor [DirectX Math Support APIs], XMBYTE4 constructor [DirectX Math Support APIs],XMBYTE4 structure, XMBYTE4 structure [DirectX Math Support APIs],XMBYTE4 constructor, XMBYTE4.XMBYTE4, XMBYTE4.XMBYTE4(uint32_t), XMBYTE4::XMBYTE4, XMBYTE4::XMBYTE4(uint32_t), dxmath.xmbyte4_ctor_6
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
 - XMBYTE4.XMBYTE4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMBYTE4::XMBYTE4(uint32_t)


## -description


Initializes a new instance of <code>XMBYTE4</code> from a <code>uint32_t</code>variable containing component data in a packed format.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419276(v=VS.85).aspx">XMBYTE4</a> from a
  <code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param Packed

The values of four vector components of the new instance, in a packed format.
      


## -remarks



The values of the four components of the new instance of <code>XMBYTE4</code> are stored in the
	argument <code>Packed</code> as follows:

<ul>
<li>
The first 8 bits (bits 0-7) of <b>Packed</b> assigned, as an unsigned integer, to the <b>x</b>member of the instance of <code>XMBYTE4</code> constructed.
	    

</li>
<li>
The second 8 bits (bits 8-15) of <b>Packed</b> assigned, as an unsigned integer, to the <b>y</b>member of the instance of <code>XMBYTE4</code> constructed.
	    

</li>
<li>
The third 8 bits (bits 16-23) of <b>Packed</b> assigned, as an unsigned
		integer, to the <b>z</b> member of the instance of <code>XMBYTE4</code>constructed.
	    

</li>
<li>
The last 8 bits (bits 24-31) of <b>Packed</b> assigned, as an unsigned integer, to the <b>w</b>member of the instance of <code>XMBYTE4</code> constructed.
	    

</li>
</ul>



## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419276(v=VS.85).aspx">XMBYTE4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415258(v=VS.85).aspx">XMBYTE4 Constructors</a>
 

 

