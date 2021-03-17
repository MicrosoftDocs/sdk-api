---
UID: NF:directxpackedvector.XMUBYTE4.XMUBYTE4(float,float,float,float)
title: XMUBYTE4::XMUBYTE4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE4 from four float arguments.
helpviewer_keywords: ["XMUBYTE4","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 structure","XMUBYTE4 structure [DirectX Math Support APIs]","XMUBYTE4 constructor","XMUBYTE4.XMUBYTE4","XMUBYTE4.XMUBYTE4(float","float","float","float)","XMUBYTE4::XMUBYTE4","XMUBYTE4::XMUBYTE4(float","float","float","float)","dxmath.xmubyte4_ctor_4"]
old-location: dxmath\xmubyte4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUBYTE4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMUBYTE4, XMUBYTE4 constructor [DirectX Math Support APIs], XMUBYTE4 constructor [DirectX Math Support APIs],XMUBYTE4 structure, XMUBYTE4 structure [DirectX Math Support APIs],XMUBYTE4 constructor, XMUBYTE4.XMUBYTE4, XMUBYTE4.XMUBYTE4(float,float,float,float), XMUBYTE4::XMUBYTE4, XMUBYTE4::XMUBYTE4(float,float,float,float), dxmath.xmubyte4_ctor_4
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

# XMUBYTE4::XMUBYTE4(float,float,float,float)


## -description

Initializes a new instance of <code>XMUBYTE4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

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

The magnitude of each argument to the constructor will be clamped to the range supported by an
	   8-bit signed integer [0, 255.0].
       

The following pseudocode demonstrates the operation of this constructor:
      


```

	XMUBYTE4 instance;

	instance.x = (uint8_t)min( max( _x, 0.0 ), 255.0 );
	instance.y = (uint8_t)min( max( _y, 0.0 ), 255.0 );
	instance.z = (uint8_t)min( max( _z, 0.0 ), 255.0 );
	instance.w = (uint8_t)min( max( _w, 0.0 ), 255.0 );

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a>



<a href="/windows/desktop/dxmath/xmubyte4-ctor">XMUBYTE4 Constructors</a>