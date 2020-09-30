---
UID: NF:directxpackedvector.XMHALF4.XMHALF4(HALF,HALF,HALF,HALF)
title: XMHALF4::XMHALF4(HALF,HALF,HALF,HALF) (directxpackedvector.h)
description: Initializes a new instance of XMHALF4 from four HALF arguments.
helpviewer_keywords: ["XMHALF4","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 constructor [DirectX Math Support APIs]","XMHALF4 structure","XMHALF4 structure [DirectX Math Support APIs]","XMHALF4 constructor","XMHALF4.XMHALF4","XMHALF4.XMHALF4(HALF","HALF","HALF","HALF)","XMHALF4::XMHALF4","XMHALF4::XMHALF4(HALF","HALF","HALF","HALF)","dxmath.xmhalf4_ctor_2"]
old-location: dxmath\xmhalf4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMHALF4.#ctor(HALF,HALF,HALF,HALF)
ms.date: 12/05/2018
ms.keywords: XMHALF4, XMHALF4 constructor [DirectX Math Support APIs], XMHALF4 constructor [DirectX Math Support APIs],XMHALF4 structure, XMHALF4 structure [DirectX Math Support APIs],XMHALF4 constructor, XMHALF4.XMHALF4, XMHALF4.XMHALF4(HALF,HALF,HALF,HALF), XMHALF4::XMHALF4, XMHALF4::XMHALF4(HALF,HALF,HALF,HALF), dxmath.xmhalf4_ctor_2
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

# XMHALF4::XMHALF4(HALF,HALF,HALF,HALF)


## -description

Initializes a new instance of <code>XMHALF4</code> from four <code>HALF</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a> from four
  <code>HALF</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

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

The following pseudocode demonstrates the operation of this constructor:
      


```

	XMHALF4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmhalf4">XMHALF4</a>



<a href="/windows/desktop/dxmath/xmhalf4-ctor">XMHALF4 Constructors</a>