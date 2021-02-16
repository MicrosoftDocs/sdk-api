---
UID: NF:directxpackedvector.XMBYTE4.XMBYTE4(float,float,float,float)
title: XMBYTE4::XMBYTE4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTE4 from four float arguments.
helpviewer_keywords: ["XMBYTE4","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 structure","XMBYTE4 structure [DirectX Math Support APIs]","XMBYTE4 constructor","XMBYTE4.XMBYTE4","XMBYTE4.XMBYTE4(float","float","float","float)","XMBYTE4::XMBYTE4","XMBYTE4::XMBYTE4(float","float","float","float)","dxmath.xmbyte4_ctor_4"]
old-location: dxmath\xmbyte4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTE4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMBYTE4, XMBYTE4 constructor [DirectX Math Support APIs], XMBYTE4 constructor [DirectX Math Support APIs],XMBYTE4 structure, XMBYTE4 structure [DirectX Math Support APIs],XMBYTE4 constructor, XMBYTE4.XMBYTE4, XMBYTE4.XMBYTE4(float,float,float,float), XMBYTE4::XMBYTE4, XMBYTE4::XMBYTE4(float,float,float,float), dxmath.xmbyte4_ctor_4
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
 - XMBYTE4::XMBYTE4
 - directxpackedvector/XMBYTE4::XMBYTE4
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
 - XMBYTE4.XMBYTE4
---

# XMBYTE4::XMBYTE4(float,float,float,float)


## -description

Initializes a new instance of <code>XMBYTE4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new 
          <code>XMBYTE4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new 
          <code>XMBYTE4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new 
          <code>XMBYTE4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new 
          <code>XMBYTE4</code> instance.

## -remarks

The magnitude of each argument to the constructor will be clamped to the range supported by an
	   8-bit signed integer [-127.0, 127.0].
       

The following pseudocode demonstrates the operation of this constructor:
      


```

	XMBYTE4 instance;

	instance.x = (int8_t)min( max( _x, -127.0 ), 127.0 );
	instance.y = (int8_t)min( max( _y, -127.0 ), 127.0 );
	instance.z = (int8_t)min( max( _z, -127.0 ), 127.0 );
	instance.w = (int8_t)min( max( _w, -127.0 ), 127.0 );

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a>



<a href="/windows/desktop/dxmath/xmbyte4-ctor">XMBYTE4 Constructors</a>