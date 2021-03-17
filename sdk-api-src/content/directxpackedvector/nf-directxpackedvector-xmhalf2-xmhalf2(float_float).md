---
UID: NF:directxpackedvector.XMHALF2.XMHALF2(float,float)
title: XMHALF2::XMHALF2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMHALF2 from two float arguments.
helpviewer_keywords: ["XMHALF2","XMHALF2 constructor [DirectX Math Support APIs]","XMHALF2 constructor [DirectX Math Support APIs]","XMHALF2 structure","XMHALF2 structure [DirectX Math Support APIs]","XMHALF2 constructor","XMHALF2.XMHALF2","XMHALF2.XMHALF2(float","float)","XMHALF2::XMHALF2","XMHALF2::XMHALF2(float","float)","dxmath.xmhalf2_ctor_4"]
old-location: dxmath\xmhalf2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMHALF2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMHALF2, XMHALF2 constructor [DirectX Math Support APIs], XMHALF2 constructor [DirectX Math Support APIs],XMHALF2 structure, XMHALF2 structure [DirectX Math Support APIs],XMHALF2 constructor, XMHALF2.XMHALF2, XMHALF2.XMHALF2(float,float), XMHALF2::XMHALF2, XMHALF2::XMHALF2(float,float), dxmath.xmhalf2_ctor_4
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
 - XMHALF2::XMHALF2
 - directxpackedvector/XMHALF2::XMHALF2
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
 - XMHALF2.XMHALF2
---

# XMHALF2::XMHALF2(float,float)


## -description

Initializes a new instance of <code>XMHALF2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf2">XMHALF2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMHALF2</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMHALF2</code> instance.

## -remarks

If the magnitude of one of this constructor's floating point arguments cannot be
	    represented by the <code>HALF</code> type, the corresponding member of the new instance of
	    <code>XMHALF2</code> will be infinity for a 16-bit integer (+0x7FFF).
	

The following pseudocode demonstrates the operation of this constructor using the XNA
	    Math <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalf">XMConvertFloatToHalf</a> function:
	


```

	XMHALF2 instance;

	instance.x = XMConvertFloatToHalf(_x);
	instance.y = XMConvertFloatToHalf(_y);
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf2">XMHALF2</a>



<a href="/windows/desktop/dxmath/xmhalf2-ctor">XMHALF2 Constructors</a>