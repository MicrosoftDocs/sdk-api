---
UID: NF:directxpackedvector.XMUBYTEN4.XMUBYTEN4(uint32_t)
title: XMUBYTEN4::XMUBYTEN4(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTEN4 from a uint32_tvariable containing component data in a packed format.
helpviewer_keywords: ["XMUBYTEN4","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 structure","XMUBYTEN4 structure [DirectX Math Support APIs]","XMUBYTEN4 constructor","XMUBYTEN4.XMUBYTEN4","XMUBYTEN4.XMUBYTEN4(uint32_t)","XMUBYTEN4::XMUBYTEN4","XMUBYTEN4::XMUBYTEN4(uint32_t)","dxmath.xmubyten4_ctor_6"]
old-location: dxmath\xmubyten4_ctor_6.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTEN4.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMUBYTEN4, XMUBYTEN4 constructor [DirectX Math Support APIs], XMUBYTEN4 constructor [DirectX Math Support APIs],XMUBYTEN4 structure, XMUBYTEN4 structure [DirectX Math Support APIs],XMUBYTEN4 constructor, XMUBYTEN4.XMUBYTEN4, XMUBYTEN4.XMUBYTEN4(uint32_t), XMUBYTEN4::XMUBYTEN4, XMUBYTEN4::XMUBYTEN4(uint32_t), dxmath.xmubyten4_ctor_6
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
 - XMUBYTEN4::XMUBYTEN4
 - directxpackedvector/XMUBYTEN4::XMUBYTEN4
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
 - XMUBYTEN4.XMUBYTEN4
---

# XMUBYTEN4::XMUBYTEN4(uint32_t)


## -description

Initializes a new instance of <code>XMUBYTEN4</code> from a <code>uint32_t</code> variable containing component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/552002c1-0000-44a6-9f43-9c958a8d1aa3">XMUBYTEN4 
	</a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param Packed

The values of four vector components of the new instance, in a packed format.

## -remarks

The values defining the three components of the new instance of <code>XMUBYTEN4</code> are
	    not normalized, and are stored in the argument <code>Packed</code> in the following
	    format:
	

<ul>
<li>
The first 8 bits (bits 0-7) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>x</b> member of the instance of <code>XMUBYTEN4</code> constructed.
		

</li>
<li>
The second 8 bits (bits 8-15) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>y</b> member of the instance of <code>XMUBYTEN4</code> constructed.
		

</li>
<li>
The third 8 bits (bits 16-23) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>z</b> member of the instance of <code>XMUBYTEN4</code> constructed.
		

</li>
<li>
The last 8 bits (bits 24-31) of <b>Packed</b> assigned, as an unsigned
		    integer, to the <b>w</b> member of the instance of <code>XMUBYTEN4</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a>



<a href="/windows/desktop/dxmath/xmubyten4-ctor">XMUBYTEN4 Constructors</a>