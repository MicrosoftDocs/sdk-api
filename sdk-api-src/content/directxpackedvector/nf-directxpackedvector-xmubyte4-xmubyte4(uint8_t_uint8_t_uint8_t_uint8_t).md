---
UID: NF:directxpackedvector.XMUBYTE4.XMUBYTE4(uint8_t,uint8_t,uint8_t,uint8_t)
title: XMUBYTE4::XMUBYTE4(uint8_t,uint8_t,uint8_t,uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE4 from four int8_t arguments.
helpviewer_keywords: ["XMUBYTE4","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 structure","XMUBYTE4 structure [DirectX Math Support APIs]","XMUBYTE4 constructor","XMUBYTE4.XMUBYTE4","XMUBYTE4.XMUBYTE4(uint8_t","uint8_t","uint8_t","uint8_t)","XMUBYTE4::XMUBYTE4","XMUBYTE4::XMUBYTE4(uint8_t","uint8_t","uint8_t","uint8_t)","dxmath.xmubyte4_ctor_3"]
old-location: dxmath\xmubyte4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTE4.#ctor(uint8_t,uint8_t,uint8_t,uint8_t)
ms.date: 12/05/2018
ms.keywords: XMUBYTE4, XMUBYTE4 constructor [DirectX Math Support APIs], XMUBYTE4 constructor [DirectX Math Support APIs],XMUBYTE4 structure, XMUBYTE4 structure [DirectX Math Support APIs],XMUBYTE4 constructor, XMUBYTE4.XMUBYTE4, XMUBYTE4.XMUBYTE4(uint8_t,uint8_t,uint8_t,uint8_t), XMUBYTE4::XMUBYTE4, XMUBYTE4::XMUBYTE4(uint8_t,uint8_t,uint8_t,uint8_t), dxmath.xmubyte4_ctor_3
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
 - XMUBYTE4::XMUBYTE4
 - directxpackedvector/XMUBYTE4::XMUBYTE4
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
 - XMUBYTE4.XMUBYTE4
---

# XMUBYTE4::XMUBYTE4(uint8_t,uint8_t,uint8_t,uint8_t)


## -description

Initializes a new instance of <code>XMUBYTE4</code> from four <code>int8_t</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a> from four
	<code>uint8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUBYTE4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUBYTE4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMUBYTE4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMUBYTE4</code> instance.

## -remarks

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUBYTE4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a>



<a href="/windows/desktop/dxmath/xmubyte4-ctor">XMUBYTE4 Constructors</a>