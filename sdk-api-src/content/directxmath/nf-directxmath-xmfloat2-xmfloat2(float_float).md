---
UID: NF:directxmath.XMFLOAT2.XMFLOAT2(float,float)
title: XMFLOAT2::XMFLOAT2(float,float) (directxmath.h)
description: Initializes a new instance of XMFLOAT2 from two float arguments.
helpviewer_keywords: ["XMFLOAT2","XMFLOAT2 constructor [DirectX Math Support APIs]","XMFLOAT2 constructor [DirectX Math Support APIs]","XMFLOAT2 structure","XMFLOAT2 structure [DirectX Math Support APIs]","XMFLOAT2 constructor","XMFLOAT2.XMFLOAT2","XMFLOAT2.XMFLOAT2(float","float)","XMFLOAT2::XMFLOAT2","XMFLOAT2::XMFLOAT2(float","float)","dxmath.xmfloat2_ctor_2"]
old-location: dxmath\xmfloat2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT2, XMFLOAT2 constructor [DirectX Math Support APIs], XMFLOAT2 constructor [DirectX Math Support APIs],XMFLOAT2 structure, XMFLOAT2 structure [DirectX Math Support APIs],XMFLOAT2 constructor, XMFLOAT2.XMFLOAT2, XMFLOAT2.XMFLOAT2(float,float), XMFLOAT2::XMFLOAT2, XMFLOAT2::XMFLOAT2(float,float), dxmath.xmfloat2_ctor_2
req.header: directxmath.h
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
req.namespace: Use DirectX.
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
 - XMFLOAT2::XMFLOAT2
 - directxmath/XMFLOAT2::XMFLOAT2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMFLOAT2.XMFLOAT2
---

# XMFLOAT2::XMFLOAT2(float,float)


## -description

Initializes a new instance of <code>XMFLOAT2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMFLOAT2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMFLOAT2</code> instance.

## -remarks

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMFLOAT2 instance;

	instance.x = _x;
	instance.y = _y;

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmfloat2-xmfloat2(constfloat)">XMFLOAT2 Constructors</a>