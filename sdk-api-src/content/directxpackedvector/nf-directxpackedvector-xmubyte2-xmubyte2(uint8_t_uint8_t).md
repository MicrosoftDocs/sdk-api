---
UID: NF:directxpackedvector.XMUBYTE2.XMUBYTE2(uint8_t,uint8_t)
title: XMUBYTE2::XMUBYTE2(uint8_t,uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE2 from two int8_t arguments.
helpviewer_keywords: ["XMUBYTE2","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 structure","XMUBYTE2 structure [DirectX Math Support APIs]","XMUBYTE2 constructor","XMUBYTE2.XMUBYTE2","XMUBYTE2.XMUBYTE2(uint8_t","uint8_t)","XMUBYTE2::XMUBYTE2","XMUBYTE2::XMUBYTE2(uint8_t","uint8_t)","dxmath.xmubyte2_ctor_3"]
old-location: dxmath\xmubyte2_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTE2.#ctor(uint8_t,uint8_t)
ms.date: 12/05/2018
ms.keywords: XMUBYTE2, XMUBYTE2 constructor [DirectX Math Support APIs], XMUBYTE2 constructor [DirectX Math Support APIs],XMUBYTE2 structure, XMUBYTE2 structure [DirectX Math Support APIs],XMUBYTE2 constructor, XMUBYTE2.XMUBYTE2, XMUBYTE2.XMUBYTE2(uint8_t,uint8_t), XMUBYTE2::XMUBYTE2, XMUBYTE2::XMUBYTE2(uint8_t,uint8_t), dxmath.xmubyte2_ctor_3
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
 - XMUBYTE2::XMUBYTE2
 - directxpackedvector/XMUBYTE2::XMUBYTE2
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
 - XMUBYTE2.XMUBYTE2
---

# XMUBYTE2::XMUBYTE2(uint8_t,uint8_t)


## -description

Initializes a new instance of <code>XMUBYTE2</code> from two <code>int8_t</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a> from two <code>uint8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMUBYTE2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMUBYTE2</code> instance.

## -remarks

The following pseudocode demonstrates the operation of this constructor:


```

	XMUBYTE2 instance;

	instance.x = _x;
	instance.y = _y;
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a>



<a href="/windows/desktop/dxmath/xmubyte2-ctor">XMUBYTE2 Constructors</a>