---
UID: NF:directxpackedvector.XMU565.XMU565(uint16_t)
title: XMU565::XMU565(uint16_t) (directxpackedvector.h)
description: Initializes a new instance of XMU565 from a uint16_t variable containing component data in a packed format.
helpviewer_keywords: ["XMU565","XMU565 constructor [DirectX Math Support APIs]","XMU565 constructor [DirectX Math Support APIs]","XMU565 structure","XMU565 structure [DirectX Math Support APIs]","XMU565 constructor","XMU565.XMU565","XMU565.XMU565(uint16_t)","XMU565::XMU565","XMU565::XMU565(uint16_t)","dxmath.xmu565_ctor_2"]
old-location: dxmath\xmu565_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMU565.#ctor(uint16_t)
ms.date: 12/05/2018
ms.keywords: XMU565, XMU565 constructor [DirectX Math Support APIs], XMU565 constructor [DirectX Math Support APIs],XMU565 structure, XMU565 structure [DirectX Math Support APIs],XMU565 constructor, XMU565.XMU565, XMU565.XMU565(uint16_t), XMU565::XMU565, XMU565::XMU565(uint16_t), dxmath.xmu565_ctor_2
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
 - XMU565::XMU565
 - directxpackedvector/XMU565::XMU565
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
 - XMU565.XMU565
---

# XMU565::XMU565(uint16_t)


## -description

Initializes a new instance of <code>XMU565</code> from a <code>uint16_t</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a> from a
	<code>uint16_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param Packed

		The values of three vector components in a packed format.

## -remarks

The values defining the three components of the new instance of <code>XMU565</code> are
	    stored in the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 5 bits (bits 0-4) of <b>Packed</b> assigned, as an integer, to the
		    <b>x</b> member of the instance of <code>XMU565</code> constructed.
		

</li>
<li>
The second 6 bits (bits 5-10) of <b>Packed</b> assigned, as an integer, to
		    the <b>y</b> member of the instance of <code>XMU565</code> constructed.
		

</li>
<li>
The third 5 bits (bits 11-15) of <b>Packed</b> assigned, as an integer, to
		    the <b>z</b> member of the instance of <code>XMU565</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmu565">XMU565</a>



<a href="/windows/desktop/dxmath/xmu565-ctor">XMU565 Constructors</a>