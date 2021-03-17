---
UID: NF:directxpackedvector.XMU555.XMU555(uint16_t)
title: XMU555::XMU555(uint16_t) (directxpackedvector.h)
description: Initializes a new instance of XMU555 from a uint16_t variable containing component data in a packed format.
helpviewer_keywords: ["XMU555","XMU555 constructor [DirectX Math Support APIs]","XMU555 constructor [DirectX Math Support APIs]","XMU555 structure","XMU555 structure [DirectX Math Support APIs]","XMU555 constructor","XMU555.XMU555","XMU555.XMU555(uint16_t)","XMU555::XMU555","XMU555::XMU555(uint16_t)","dxmath.xmu555_ctor_2"]
old-location: dxmath\xmu555_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU555.#ctor(uint16_t)
ms.date: 12/05/2018
ms.keywords: XMU555, XMU555 constructor [DirectX Math Support APIs], XMU555 constructor [DirectX Math Support APIs],XMU555 structure, XMU555 structure [DirectX Math Support APIs],XMU555 constructor, XMU555.XMU555, XMU555.XMU555(uint16_t), XMU555::XMU555, XMU555::XMU555(uint16_t), dxmath.xmu555_ctor_2
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
 - XMU555::XMU555
 - directxpackedvector/XMU555::XMU555
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
 - XMU555.XMU555
---

# XMU555::XMU555(uint16_t)


## -description

Initializes a new instance of <code>XMU555</code> from a <code>uint16_t</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a> from a
	<code>uint16_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of four vector components in a packed format.

## -remarks

The values defining the four components of the new instance of <code>XMU555</code> are
	    stored in the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 5 bits (bits 0-4) of <b>Packed</b> assigned, as an integer, to the
		    <b>x</b> member of the instance of <code>XMU555</code> constructed.
		

</li>
<li>
The second 5 bits (bits 5-9) of <b>Packed</b> assigned, as an integer, to
		    the <b>y</b> member of the instance of <code>XMU555</code> constructed.
		

</li>
<li>
The third 5 bits (bits 10-14) of <b>Packed</b> assigned, as an integer, to
		    the <b>z</b> member of the instance of <code>XMU555</code> constructed.
		

</li>
<li>
The last 1 bits (bit 15) of <b>Packed</b> assigned, as an integer, to
		    the <b>w</b> member of the instance of <code>XMU555</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu555">XMU555</a>



<a href="/windows/desktop/dxmath/xmu555-ctor">XMU555 Constructors</a>