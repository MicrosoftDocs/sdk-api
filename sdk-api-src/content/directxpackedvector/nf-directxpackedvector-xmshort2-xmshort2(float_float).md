---
UID: NF:directxpackedvector.XMSHORT2.XMSHORT2(float,float)
title: XMSHORT2::XMSHORT2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT2 from two float arguments.
helpviewer_keywords: ["XMSHORT2","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 structure","XMSHORT2 structure [DirectX Math Support APIs]","XMSHORT2 constructor","XMSHORT2.XMSHORT2","XMSHORT2.XMSHORT2(float","float)","XMSHORT2::XMSHORT2","XMSHORT2::XMSHORT2(float","float)","dxmath.xmshort2_ctor_4"]
old-location: dxmath\xmshort2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORT2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMSHORT2, XMSHORT2 constructor [DirectX Math Support APIs], XMSHORT2 constructor [DirectX Math Support APIs],XMSHORT2 structure, XMSHORT2 structure [DirectX Math Support APIs],XMSHORT2 constructor, XMSHORT2.XMSHORT2, XMSHORT2.XMSHORT2(float,float), XMSHORT2::XMSHORT2, XMSHORT2::XMSHORT2(float,float), dxmath.xmshort2_ctor_4
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
 - XMSHORT2::XMSHORT2
 - directxpackedvector/XMSHORT2::XMSHORT2
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
 - XMSHORT2.XMSHORT2
---

# XMSHORT2::XMSHORT2(float,float)


## -description

Initializes a new instance of <code>XMSHORT2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORT2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORT2</code> instance.

## -remarks

The magnitude of each argument to the constructor will be clamped to the range supported
	    by a 16-bit signed integer [-32767.0, 32767.0].
	

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMSHORT2 instance;

	instance.x = (int16_t)min( max( _x, -32767.0 ), 32767.0 );
	instance.y = (int16_t)min( max( _y, -32767.0 ), 32767.0 );
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a>



<a href="/windows/desktop/dxmath/xmshort2-ctor">XMSHORT2 Constructors</a>