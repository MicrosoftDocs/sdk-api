---
UID: NF:directxpackedvector.XMSHORT4.XMSHORT4(int16_t,int16_t,int16_t,int16_t)
title: XMSHORT4::XMSHORT4(int16_t,int16_t,int16_t,int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT4 from four int16_t arguments.
helpviewer_keywords: ["XMSHORT4","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 structure","XMSHORT4 structure [DirectX Math Support APIs]","XMSHORT4 constructor","XMSHORT4.XMSHORT4","XMSHORT4.XMSHORT4(int16_t","int16_t","int16_t","int16_t)","XMSHORT4::XMSHORT4","XMSHORT4::XMSHORT4(int16_t","int16_t","int16_t","int16_t)","dxmath.xmshort4_ctor_2"]
old-location: dxmath\xmshort4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORT4.#ctor(int16_t,int16_t,int16_t,int16_t)
ms.date: 12/05/2018
ms.keywords: XMSHORT4, XMSHORT4 constructor [DirectX Math Support APIs], XMSHORT4 constructor [DirectX Math Support APIs],XMSHORT4 structure, XMSHORT4 structure [DirectX Math Support APIs],XMSHORT4 constructor, XMSHORT4.XMSHORT4, XMSHORT4.XMSHORT4(int16_t,int16_t,int16_t,int16_t), XMSHORT4::XMSHORT4, XMSHORT4::XMSHORT4(int16_t,int16_t,int16_t,int16_t), dxmath.xmshort4_ctor_2
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
 - XMSHORT4::XMSHORT4
 - directxpackedvector/XMSHORT4::XMSHORT4
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
 - XMSHORT4.XMSHORT4
---

# XMSHORT4::XMSHORT4(int16_t,int16_t,int16_t,int16_t)


## -description

Initializes a new instance of <code>XMSHORT4</code> from four <code>int16_t</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> from four
	<code>int16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORT4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORT4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMSHORT4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMSHORT4</code> instance.

## -remarks

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMSHORT4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a>



<a href="/windows/desktop/dxmath/xmshort4-ctor">XMSHORT4 Constructors</a>