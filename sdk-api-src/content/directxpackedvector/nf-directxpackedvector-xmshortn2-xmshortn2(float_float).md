---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(float,float)
title: XMSHORTN2::XMSHORTN2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMSHORTN2 from two normalized floatarguments.
helpviewer_keywords: ["XMSHORTN2","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 structure","XMSHORTN2 structure [DirectX Math Support APIs]","XMSHORTN2 constructor","XMSHORTN2.XMSHORTN2","XMSHORTN2.XMSHORTN2(float","float)","XMSHORTN2::XMSHORTN2","XMSHORTN2::XMSHORTN2(float","float)","dxmath.xmshortn2_ctor_4"]
old-location: dxmath\xmshortn2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORTN2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMSHORTN2, XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2, XMSHORTN2.XMSHORTN2(float,float), XMSHORTN2::XMSHORTN2, XMSHORTN2::XMSHORTN2(float,float), dxmath.xmshortn2_ctor_4
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
 - XMSHORTN2::XMSHORTN2
 - directxpackedvector/XMSHORTN2::XMSHORTN2
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
 - XMSHORTN2.XMSHORTN2
---

# XMSHORTN2::XMSHORTN2(float,float)


## -description

Initializes a new instance of <code>XMSHORTN2</code> from two normalized <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> from two
	normalized <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

A normalized value for the x-coordinate of the vector.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMSHORTN2</code>, it is multiplied by <code>32767.0f</code> and
		    then stored as the <b>x</b> member of the structure.

### -param _y

A normalized value for the y-coordinate of the vector, the <b>y</b> of the
		    new instance of <code>XMSHORTN2</code>.
		

This argument should be between -1.0 and 1.0; during the instantiation of an
		    instance of <code>XMSHORTN2</code>, it is multiplied by <code>32767.0f</code> and
		    then stored as the <b>y</b> member of the structure.

## -remarks

All input values,<i>_x</i> and <i>_y</i> are clamped to a range of -1.0 to 1.0.
	

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMSHORTN2 instance;
	_x1=min( max( _x, -1.0 ), 1.0 );
	_y1=min( max( _y, -1.0 ), 1.0 );
	_x1 = round( _x1 * 32767.0f);
	_y1 = round( _y1 * 32767.0f);
	instance._x = _x1;
	instance._y = _y1;
	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a>



<a href="/windows/desktop/dxmath/xmshortn2-ctor">XMSHORTN2 Constructors</a>