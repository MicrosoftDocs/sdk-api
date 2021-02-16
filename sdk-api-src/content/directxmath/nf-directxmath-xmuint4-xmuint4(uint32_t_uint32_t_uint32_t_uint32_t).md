---
UID: NF:directxmath.XMUINT4.XMUINT4(uint32_t,uint32_t,uint32_t,uint32_t)
title: XMUINT4::XMUINT4(uint32_t,uint32_t,uint32_t,uint32_t) (directxmath.h)
description: Initializes a new instance of XMUINT4 from four uint32_t arguments.
helpviewer_keywords: ["XMUINT4","XMUINT4 constructor [DirectX Math Support APIs]","XMUINT4 constructor [DirectX Math Support APIs]","XMUINT4 structure","XMUINT4 structure [DirectX Math Support APIs]","XMUINT4 constructor","XMUINT4.XMUINT4","XMUINT4.XMUINT4(uint32_t","uint32_t","uint32_t","uint32_t)","XMUINT4::XMUINT4","XMUINT4::XMUINT4(uint32_t","uint32_t","uint32_t","uint32_t)","dxmath.xmuint4_ctor_2"]
old-location: dxmath\xmuint4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUINT4.#ctor(uint32_t,uint32_t,uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: XMUINT4, XMUINT4 constructor [DirectX Math Support APIs], XMUINT4 constructor [DirectX Math Support APIs],XMUINT4 structure, XMUINT4 structure [DirectX Math Support APIs],XMUINT4 constructor, XMUINT4.XMUINT4, XMUINT4.XMUINT4(uint32_t,uint32_t,uint32_t,uint32_t), XMUINT4::XMUINT4, XMUINT4::XMUINT4(uint32_t,uint32_t,uint32_t,uint32_t), dxmath.xmuint4_ctor_2
req.header: directxmath.h
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
req.namespace: Use DirectX.
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
 - XMUINT4::XMUINT4
 - directxmath/XMUINT4::XMUINT4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMUINT4.XMUINT4
---

# XMUINT4::XMUINT4(uint32_t,uint32_t,uint32_t,uint32_t)


## -description

Initializes a new instance of <code>XMUINT4</code> from four <code>uint32_t</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint4">XMUINT4</a> from four
	<code>uint32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUINT4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUINT4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUINT4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUINT4</code> instance.

## -remarks

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUINT4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint4">XMUINT4</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmuint4-xmuint4(constuint32_t)">XMUINT4 Constructors</a>