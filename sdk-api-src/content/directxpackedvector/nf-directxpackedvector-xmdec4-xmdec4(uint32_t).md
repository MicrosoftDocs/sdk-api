---
UID: NF:directxpackedvector.XMDEC4.XMDEC4(uint32_t)
title: XMDEC4::XMDEC4(uint32_t) (directxpackedvector.h)
description: Initializes a new instance of XMDEC4 from a uint32_t variable containing component data in a packed format.
helpviewer_keywords: ["XMDEC4","XMDEC4 constructor [DirectX Math Support APIs]","XMDEC4 constructor [DirectX Math Support APIs]","XMDEC4 structure","XMDEC4 structure [DirectX Math Support APIs]","XMDEC4 constructor","XMDEC4.XMDEC4","XMDEC4.XMDEC4(uint32_t)","XMDEC4::XMDEC4","XMDEC4::XMDEC4(uint32_t)","dxmath.xmdec4_ctor_2"]
old-location: dxmath\xmdec4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMDEC4.#ctor(uint32_t)
ms.date: 12/05/2018
ms.keywords: XMDEC4, XMDEC4 constructor [DirectX Math Support APIs], XMDEC4 constructor [DirectX Math Support APIs],XMDEC4 structure, XMDEC4 structure [DirectX Math Support APIs],XMDEC4 constructor, XMDEC4.XMDEC4, XMDEC4.XMDEC4(uint32_t), XMDEC4::XMDEC4, XMDEC4::XMDEC4(uint32_t), dxmath.xmdec4_ctor_2
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
 - XMDEC4::XMDEC4
 - directxpackedvector/XMDEC4::XMDEC4
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
 - XMDEC4.XMDEC4
---

# XMDEC4::XMDEC4(uint32_t)


## -description

Initializes a new instance of <code>XMDEC4</code> from a <code>uint32_t</code> variable containing
	component data in a packed format.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/a52fa5e4-ee45-4256-a06a-6984d63b5578">XMDEC4 
	</a> from a
	<code>uint32_t</code> variable containing component data in a packed format.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param Packed

The values of the four components of the new instance of <code>XMDEC4</code> are
		    stored in the argument <code>Packed</code> as follows:

## -remarks

The values of the four components of the new instance of <code>XMDEC4</code> are stored in
	    the argument <code>Packed</code> as follows:
	

<ul>
<li>
The first 10 bits (bits 0-9) of <b>Packed</b> assigned, as an integer, to
		    the <b>x</b> member of the instance of <code>XMDEC4</code> constructed.
		

</li>
<li>
The second 10 bits (bits 10-19) of <b>Packed</b> assigned, as an integer, to
		    the <b>y</b> member of the instance of <code>XMDEC4</code> constructed.
		

</li>
<li>
The third 10 bits (bits 20-29) of <b>Packed</b> assigned, as an integer, to
		    the <b>z</b> member of the instance of <code>XMDEC4</code> constructed.
		

</li>
<li>
The last 2 bits (bits 30-31) of <b>Packed</b> assigned, as an integer, to
		    the <b>w</b> member of the instance of <code>XMDEC4</code> constructed.
		

</li>
</ul>

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmdec4">XMDEC4</a>



<a href="/windows/desktop/dxmath/xmdec4-ctor">XMDEC4 Constructors</a>