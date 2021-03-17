---
UID: NF:directxpackedvector.XMXDEC4.XMXDEC4(uint32_t)
title: XMXDEC4::XMXDEC4(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMXDEC4 from a uint32_t6 variable containing component data in a packed format.
helpviewer_keywords: ["XMXDEC4","XMXDEC4 constructor [DirectX Math Support APIs]","XMXDEC4 constructor [DirectX Math Support APIs]","XMXDEC4 structure","XMXDEC4 structure [DirectX Math Support APIs]","XMXDEC4 constructor","XMXDEC4.XMXDEC4","XMXDEC4.XMXDEC4(uint32_t)","XMXDEC4::XMXDEC4","XMXDEC4::XMXDEC4(uint32_t)","dxmath.xmxdec4_ctor_2"]
old-location: dxmath\xmxdec4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMXDEC4.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMXDEC4, XMXDEC4 constructor [DirectX Math Support APIs], XMXDEC4 constructor [DirectX Math Support APIs],XMXDEC4 structure, XMXDEC4 structure [DirectX Math Support APIs],XMXDEC4 constructor, XMXDEC4.XMXDEC4, XMXDEC4.XMXDEC4(uint32_t), XMXDEC4::XMXDEC4, XMXDEC4::XMXDEC4(uint32_t), dxmath.xmxdec4_ctor_2
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
 - XMXDEC4::XMXDEC4
 - directxpackedvector/XMXDEC4::XMXDEC4
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
 - XMXDEC4.XMXDEC4
---

# XMXDEC4::XMXDEC4(uint32_t)


## -description

Initializes a new instance of <code>XMXDEC4</code> from a <code>uint32_t6</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/5b46e0fb-e4a5-49c4-8084-0c631d43d4f7">XMXDEC4
	</a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of the four components of the new instance of <code>XMXDEC4</code> are
		    stored in the argument <code>Packed</code> as follows:

## -remarks

The values of the four components of the new instance of <code>XMXDEC4</code> are stored in
	    the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 10 bits (bits 0-9) of <b>Packed</b> assigned, as an integer, to
		    the <b>x</b> member of the instance of <code>XMXDEC4</code> constructed.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned, as an integer, to
		    the <b>y</b> member of the instance of <code>XMXDEC4</code> constructed.
		

</li>
<li>
The third 10 bits (bits 20-29) of <b>Packed</b> assigned, as an integer, to
		    the <b>z</b> member of the instance of <code>XMXDEC4</code> constructed.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned, as an unsigned integer, to
		    the <b>w</b> member of the instance of <code>XMXDEC4</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmxdec4">XMXDEC4</a>



<a href="/windows/desktop/dxmath/xmxdec4-ctor">XMXDEC4 Constructors</a>