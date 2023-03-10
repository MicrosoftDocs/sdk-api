---
UID: NF:directxpackedvector.XMCOLOR.XMCOLOR(float,float,float,float)
title: XMCOLOR::XMCOLOR(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMCOLOR from four float arguments.
helpviewer_keywords: ["XMCOLOR","XMCOLOR constructor [DirectX Math Support APIs]","XMCOLOR constructor [DirectX Math Support APIs]","XMCOLOR structure","XMCOLOR structure [DirectX Math Support APIs]","XMCOLOR constructor","XMCOLOR.XMCOLOR","XMCOLOR.XMCOLOR(float","float","float","float)","XMCOLOR::XMCOLOR","XMCOLOR::XMCOLOR(float","float","float","float)","dxmath.xmcolor_ctor_3"]
old-location: dxmath\xmcolor_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMCOLOR.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMCOLOR, XMCOLOR constructor [DirectX Math Support APIs], XMCOLOR constructor [DirectX Math Support APIs],XMCOLOR structure, XMCOLOR structure [DirectX Math Support APIs],XMCOLOR constructor, XMCOLOR.XMCOLOR, XMCOLOR.XMCOLOR(float,float,float,float), XMCOLOR::XMCOLOR, XMCOLOR::XMCOLOR(float,float,float,float), dxmath.xmcolor_ctor_3
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
 - XMCOLOR::XMCOLOR
 - directxpackedvector/XMCOLOR::XMCOLOR
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
 - XMCOLOR.XMCOLOR
---

# XMCOLOR::XMCOLOR(float,float,float,float)


## -description

Initializes a new instance of <code>XMCOLOR</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR </a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _r

Normalized value for the <i>red</i> channel of a 32-bit ARGB color
		    stored in the new instance of <code>XMCOLOR</code>. The value of this argument
		    should be in the range [0.0 - 1.0].

### -param _g

Normalized value for the <i>green</i> channel of a 32-bit ARGB
		    color stored in the new instance of <code>XMCOLOR</code>. The value of this
		    argument should be in the range [0.0 - 1.0].

### -param _b

Normalized value for the <i>blue</i> channel of a 32-bit ARGB
		    color stored in the new instance of <code>XMCOLOR</code>. The value of this
		    argument should be in the range [0.0 - 1.0].

### -param _a

Normalized value for the <i>alpha</i> channel of a 32-bit ARGB
		    color stored in the new instance of <code>XMCOLOR</code>. The value of this
		    argument should be in the range [0.0 - 1.0].

## -remarks

During the instantiation of an instance of <code>XMCOLOR</code>, all input arguments to
	    this constructor are clamped to a range of [0.0, 1.0], multiplied by <code>255.0f</code>,
	    as well as rounded, and before being stored in the appropriate structure member.
	  

The following pseudocode demonstrates the operation of this constructor, which takes
	    advantage of the <code>union</code> of the four components of the <code>XMCOLOR</code> vector with an instance of <code>uint32_t</code> in the definition of the structure:
	  


```

        XMCOLOR instance;        
	_a1 = min( max( _a, 0.0 ), 1.0 );
	_r1 = min( max( _r, 0.0 ), 1.0 );
	_g1 = min( max( _g, 0.0 ), 1.0 );
	_b1 = min( max( _b, 0.0 ), 1.0 );

	_a1 = round ( _a1 * 255.0f );
	_r1 = round ( _r1 * 255.0f );
	_g1 = round ( _g1 * 255.0f );
	_b1 = round ( _b1 * 255.0f );

	instance.v =  ( (uint32_t)_a1  << 24) |
                      ( (uint32_t)_r1  << 16) |
                      ( (uint32_t)_g1  <<  8) |
                      ( (uint32_t)_b1 );
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmcolor">XMCOLOR</a>



<a href="/windows/desktop/dxmath/xmcolor-ctor">XMCOLOR Constructors</a>