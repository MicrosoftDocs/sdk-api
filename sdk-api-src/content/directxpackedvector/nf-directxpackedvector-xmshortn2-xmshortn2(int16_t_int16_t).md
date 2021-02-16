---
UID: NF:directxpackedvector.XMSHORTN2.XMSHORTN2(int16_t,int16_t)
title: XMSHORTN2::XMSHORTN2(int16_t,int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORTN2 from two int16_t arguments.
helpviewer_keywords: ["XMSHORTN2","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 constructor [DirectX Math Support APIs]","XMSHORTN2 structure","XMSHORTN2 structure [DirectX Math Support APIs]","XMSHORTN2 constructor","XMSHORTN2.XMSHORTN2","XMSHORTN2.XMSHORTN2(int16_t","int16_t)","XMSHORTN2::XMSHORTN2","XMSHORTN2::XMSHORTN2(int16_t","int16_t)","dxmath.xmshortn2_ctor_2"]
old-location: dxmath\xmshortn2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMSHORTN2.#ctor(int16_t,int16_t)
ms.date: 12/05/2018
ms.keywords: XMSHORTN2, XMSHORTN2 constructor [DirectX Math Support APIs], XMSHORTN2 constructor [DirectX Math Support APIs],XMSHORTN2 structure, XMSHORTN2 structure [DirectX Math Support APIs],XMSHORTN2 constructor, XMSHORTN2.XMSHORTN2, XMSHORTN2.XMSHORTN2(int16_t,int16_t), XMSHORTN2::XMSHORTN2, XMSHORTN2::XMSHORTN2(int16_t,int16_t), dxmath.xmshortn2_ctor_2
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

# XMSHORTN2::XMSHORTN2(int16_t,int16_t)


## -description

Initializes a new instance of <code>XMSHORTN2</code> from two <code>int16_t</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a> from two
	<code>int16_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMSHORTN2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMSHORTN2</code> instance.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of
	    this constructor:
	


```

	XMSHORTN2 instance;

	instance.x = _x;
	instance.y = _y;


    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshortn2">XMSHORTN2</a>



<a href="/windows/desktop/dxmath/xmshortn2-ctor">XMSHORTN2 Constructors</a>