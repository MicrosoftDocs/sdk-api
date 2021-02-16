---
UID: NF:directxpackedvector.XMUBYTEN4.XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t)
title: XMUBYTEN4::XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTEN4 from four uint8_t arguments.
helpviewer_keywords: ["XMUBYTEN4","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 structure","XMUBYTEN4 structure [DirectX Math Support APIs]","XMUBYTEN4 constructor","XMUBYTEN4.XMUBYTEN4","XMUBYTEN4.XMUBYTEN4(uint8_t","uint8_t","uint8_t","uint8_t)","XMUBYTEN4::XMUBYTEN4","XMUBYTEN4::XMUBYTEN4(uint8_t","uint8_t","uint8_t","uint8_t)","dxmath.xmubyten4_ctor_3"]
old-location: dxmath\xmubyten4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTEN4.#ctor(uint8_t,uint8_t,uint8_t,uint8_t)
ms.date: 12/05/2018
ms.keywords: XMUBYTEN4, XMUBYTEN4 constructor [DirectX Math Support APIs], XMUBYTEN4 constructor [DirectX Math Support APIs],XMUBYTEN4 structure, XMUBYTEN4 structure [DirectX Math Support APIs],XMUBYTEN4 constructor, XMUBYTEN4.XMUBYTEN4, XMUBYTEN4.XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t), XMUBYTEN4::XMUBYTEN4, XMUBYTEN4::XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t), dxmath.xmubyten4_ctor_3
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

# XMUBYTEN4::XMUBYTEN4(uint8_t,uint8_t,uint8_t,uint8_t)


## -description

Initializes a new instance of <code>XMUBYTEN4</code> from four <code>uint8_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/552002c1-0000-44a6-9f43-9c958a8d1aa3">XMUBYTEN4 
	</a> from a
	four <code>uint8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUBYTEN4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUBYTEN4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUBYTEN4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUBYTEN4</code> instance.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of
	    this constructor:
	


```

	    XMUBYTEN4 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	    instance.z = _z; 
	    instance.w = _w;

	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a>



<a href="/windows/desktop/dxmath/xmubyten4-ctor">XMUBYTEN4 Constructors</a>