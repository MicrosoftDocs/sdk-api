---
UID: NF:directxpackedvector.XMUSHORTN2.XMUSHORTN2(float,float)
title: XMUSHORTN2::XMUSHORTN2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORTN2 from two normalized floatarguments.
helpviewer_keywords: ["XMUSHORTN2","XMUSHORTN2 constructor [DirectX Math Support APIs]","XMUSHORTN2 constructor [DirectX Math Support APIs]","XMUSHORTN2 structure","XMUSHORTN2 structure [DirectX Math Support APIs]","XMUSHORTN2 constructor","XMUSHORTN2.XMUSHORTN2","XMUSHORTN2.XMUSHORTN2(float","float)","XMUSHORTN2::XMUSHORTN2","XMUSHORTN2::XMUSHORTN2(float","float)","dxmath.xmushortn2_ctor_4"]
old-location: dxmath\xmushortn2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUSHORTN2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMUSHORTN2, XMUSHORTN2 constructor [DirectX Math Support APIs], XMUSHORTN2 constructor [DirectX Math Support APIs],XMUSHORTN2 structure, XMUSHORTN2 structure [DirectX Math Support APIs],XMUSHORTN2 constructor, XMUSHORTN2.XMUSHORTN2, XMUSHORTN2.XMUSHORTN2(float,float), XMUSHORTN2::XMUSHORTN2, XMUSHORTN2::XMUSHORTN2(float,float), dxmath.xmushortn2_ctor_4
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
 - XMUSHORTN2::XMUSHORTN2
 - directxpackedvector/XMUSHORTN2::XMUSHORTN2
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
 - XMUSHORTN2.XMUSHORTN2
---

# XMUSHORTN2::XMUSHORTN2(float,float)


## -description

Initializes a new instance of <code>XMUSHORTN2</code> from two normalized <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a> from two
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUSHORTN2</code>, it is multiplied by <code>65535.0f</code> and
		    then stored as the <b>x</b> member of the structure.

### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMUSHORTN2</code>.
		

This argument should be between 0.0 and 1.0; during the instantiation of an
		    instance of <code>XMUSHORTN2</code>, it is multiplied by <code>65535.0f</code> and
		    then stored as the <b>y</b> member of the structure.

## -remarks

All input values,<i>_x</i> and <i>_y</i> are clamped to a range of 0.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUSHORTN2 instance;
	_x1=min( max( _x, 0.0 ), 1.0 );
	_y1=min( max( _y, 0.0 ), 1.0 );
	_x1 = round( _x1 * 65535.0f);
	_y1 = round( _y1 * 65535.0f);
	instance._x = _x1;
	instance._y = _y1;
	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn2">XMUSHORTN2</a>



<a href="/windows/desktop/dxmath/xmushortn2-ctor">XMUSHORTN2 Constructors</a>