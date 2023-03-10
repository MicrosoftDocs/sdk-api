---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(uint32_t)
title: XMBYTEN4::XMBYTEN4(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN4 from a uint32_tvariable containing component data in a packed format.
helpviewer_keywords: ["XMBYTEN4","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 structure","XMBYTEN4 structure [DirectX Math Support APIs]","XMBYTEN4 constructor","XMBYTEN4.XMBYTEN4","XMBYTEN4.XMBYTEN4(uint32_t)","XMBYTEN4::XMBYTEN4","XMBYTEN4::XMBYTEN4(uint32_t)","dxmath.xmbyten4_ctor_6"]
old-location: dxmath\xmbyten4_ctor_6.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN4.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMBYTEN4, XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4, XMBYTEN4.XMBYTEN4(uint32_t), XMBYTEN4::XMBYTEN4, XMBYTEN4::XMBYTEN4(uint32_t), dxmath.xmbyten4_ctor_6
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
 - XMBYTEN4::XMBYTEN4
 - directxpackedvector/XMBYTEN4::XMBYTEN4
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
 - XMBYTEN4.XMBYTEN4
---

# XMBYTEN4::XMBYTEN4(uint32_t)


## -description

Initializes a new instance of <code>XMBYTEN4</code> from a <code>uint32_t</code> variable containing component data in a packed format.
    

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
The first 8 bits (bits 0-7) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>x</b> member of the instance of <code>XMBYTEN4</code> constructed.
		

</li>
<li>
The second 8 bits (bits 8-15) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>y</b> member of the instance of <code>XMBYTEN4</code> constructed.
		

</li>
<li>
The third 8 bits (bits 16-23) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>z</b> member of the instance of <code>XMBYTEN4</code> constructed.
		

</li>
<li>
The last 8 bits (bits 24-31) of <b>Packed</b> assigned, as a signed
		    integer, to the <b>w</b> member of the instance of <code>XMBYTEN4</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>



<a href="/windows/desktop/dxmath/xmbyten4-ctor">XMBYTEN4 Constructors</a>