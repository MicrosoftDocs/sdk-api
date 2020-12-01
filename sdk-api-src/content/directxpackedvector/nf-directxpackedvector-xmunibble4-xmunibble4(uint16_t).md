---
UID: NF:directxpackedvector.XMUNIBBLE4.XMUNIBBLE4(uint16_t)
title: XMUNIBBLE4::XMUNIBBLE4(uint16_t) (directxpackedvector.h)
description: Initializes a new instance of XMUNIBBLE from a uint16_t variable containing component data in a packed format.
helpviewer_keywords: ["XMUNIBBLE4","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 structure","XMUNIBBLE4 structure [DirectX Math Support APIs]","XMUNIBBLE4 constructor","XMUNIBBLE4.XMUNIBBLE4","XMUNIBBLE4.XMUNIBBLE4(uint16_t)","XMUNIBBLE4::XMUNIBBLE4","XMUNIBBLE4::XMUNIBBLE4(uint16_t)","dxmath.xmunibble4_ctor_2"]
old-location: dxmath\xmunibble4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUNIBBLE4.#ctor(uint16_t)
ms.date: 12/05/2018
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 constructor [DirectX Math Support APIs], XMUNIBBLE4 constructor [DirectX Math Support APIs],XMUNIBBLE4 structure, XMUNIBBLE4 structure [DirectX Math Support APIs],XMUNIBBLE4 constructor, XMUNIBBLE4.XMUNIBBLE4, XMUNIBBLE4.XMUNIBBLE4(uint16_t), XMUNIBBLE4::XMUNIBBLE4, XMUNIBBLE4::XMUNIBBLE4(uint16_t), dxmath.xmunibble4_ctor_2
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
 - XMUNIBBLE4::XMUNIBBLE4
 - directxpackedvector/XMUNIBBLE4::XMUNIBBLE4
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
 - XMUNIBBLE4.XMUNIBBLE4
---

# XMUNIBBLE4::XMUNIBBLE4(uint16_t)


## -description

Initializes a new instance of <code>XMUNIBBLE</code> from a <code>uint16_t</code> variable
	  containing component data in a packed format.
  

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a> from a
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



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>



<a href="/windows/desktop/dxmath/xmunibble4-ctor">XMUNIBBLE4 Constructors</a>