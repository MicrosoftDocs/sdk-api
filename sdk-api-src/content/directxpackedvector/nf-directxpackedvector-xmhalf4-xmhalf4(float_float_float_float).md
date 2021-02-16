---
UID: NF:directxpackedvector.XMHALF4.XMHALF4(float,float,float,float)
title: XMHALF4::XMHALF4(float,float,float,float) (directxpackedvector.h)
description: Initializes a new instance of XMHALF4 from four float arguments.
helpviewer_keywords: ["XMHALF4","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 structure","XMHALF4 structure [DirectX Math Support APIs]","XMHALF4 constructor","XMHALF4.XMHALF4","XMHALF4.XMHALF4(float","float","float","float)","XMHALF4::XMHALF4","XMHALF4::XMHALF4(float","float","float","float)","dxmath.xmhalf4_ctor_4"]
old-location: dxmath\xmhalf4_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMHALF4.#ctor(float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMHALF4, XMHALF4 constructor [DirectX Math Support APIs], XMHALF4 constructor [DirectX Math Support APIs],XMHALF4 structure, XMHALF4 structure [DirectX Math Support APIs],XMHALF4 constructor, XMHALF4.XMHALF4, XMHALF4.XMHALF4(float,float,float,float), XMHALF4::XMHALF4, XMHALF4::XMHALF4(float,float,float,float), dxmath.xmhalf4_ctor_4
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
 - XMHALF4::XMHALF4
 - directxpackedvector/XMHALF4::XMHALF4
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
 - XMHALF4.XMHALF4
---

# XMHALF4::XMHALF4(float,float,float,float)


## -description

Initializes a new instance of <code>XMHALF4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMHALF4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMHALF4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMHALF4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMHALF4</code> instance.

## -remarks

If the magnitude of one of this constructor's floating point arguments cannot be
	    represented by the <code>HALF</code> type, the corresponding member of the new instance of
	    <code>XMHALF4</code> will be infinity for a 16-bit integer (+0x7FFF).
	

The following pseudocode demonstrates the operation of this constructor using the XNA
	    Math <a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalf">XMConvertFloatToHalf</a> function:
	


```

	XMHALF4 instance;

	instance.x = XMConvertFloatToHalf(_x);
	instance.y = XMConvertFloatToHalf(_y);
	instance.z = XMConvertFloatToHalf(_z);
	instance.w = XMConvertFloatToHalf(_w);

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalf">XMConvertFloatToHalf</a>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a>



<a href="/windows/desktop/dxmath/xmhalf4-ctor">XMHALF4 Constructors</a>