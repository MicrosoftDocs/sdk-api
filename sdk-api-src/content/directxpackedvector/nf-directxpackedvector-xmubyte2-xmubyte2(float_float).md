---
UID: NF:directxpackedvector.XMUBYTE2.XMUBYTE2(float,float)
title: XMUBYTE2::XMUBYTE2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE2 from two float arguments.
helpviewer_keywords: ["XMUBYTE2","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 structure","XMUBYTE2 structure [DirectX Math Support APIs]","XMUBYTE2 constructor","XMUBYTE2.XMUBYTE2","XMUBYTE2.XMUBYTE2(float","float)","XMUBYTE2::XMUBYTE2","XMUBYTE2::XMUBYTE2(float","float)","dxmath.xmubyte2_ctor_4"]
old-location: dxmath\xmubyte2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTE2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMUBYTE2, XMUBYTE2 constructor [DirectX Math Support APIs], XMUBYTE2 constructor [DirectX Math Support APIs],XMUBYTE2 structure, XMUBYTE2 structure [DirectX Math Support APIs],XMUBYTE2 constructor, XMUBYTE2.XMUBYTE2, XMUBYTE2.XMUBYTE2(float,float), XMUBYTE2::XMUBYTE2, XMUBYTE2::XMUBYTE2(float,float), dxmath.xmubyte2_ctor_4
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

# XMUBYTE2::XMUBYTE2(float,float)


## -description

Initializes a new instance of <code>XMUBYTE2</code> from two <code>float</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a> from two <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMUBYTE2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMUBYTE2</code> instance.

## -remarks

The magnitude of each argument to the constructor will be clamped to the range supported by an 8-bit signed integer [0,
   255.0].

The following pseudocode demonstrates the operation of this constructor:


```

	XMUBYTE2 instance;

	instance.x = (uint8_t)min( max( _x, 0.0 ), 255.0 );
	instance.y = (uint8_t)min( max( _y, 0.0 ), 255.0 );
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a>



<a href="/windows/desktop/dxmath/xmubyte2-ctor">XMUBYTE2 Constructors</a>