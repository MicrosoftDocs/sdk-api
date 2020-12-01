---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(int8_t,int8_t,int8_t,int8_t)
title: XMBYTEN4::XMBYTEN4(int8_t,int8_t,int8_t,int8_t) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN4 from four int8_t arguments.
helpviewer_keywords: ["XMBYTEN4","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 structure","XMBYTEN4 structure [DirectX Math Support APIs]","XMBYTEN4 constructor","XMBYTEN4.XMBYTEN4","XMBYTEN4.XMBYTEN4(int8_t","int8_t","int8_t","int8_t)","XMBYTEN4::XMBYTEN4","XMBYTEN4::XMBYTEN4(int8_t","int8_t","int8_t","int8_t)","dxmath.xmbyten4_ctor_3"]
old-location: dxmath\xmbyten4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTEN4.#ctor(int8_t,int8_t,int8_t,int8_t)
ms.date: 12/05/2018
ms.keywords: XMBYTEN4, XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4, XMBYTEN4.XMBYTEN4(int8_t,int8_t,int8_t,int8_t), XMBYTEN4::XMBYTEN4, XMBYTEN4::XMBYTEN4(int8_t,int8_t,int8_t,int8_t), dxmath.xmbyten4_ctor_3
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
 - XMBYTEN4::XMBYTEN4
 - directxpackedvector/XMBYTEN4::XMBYTEN4
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
 - XMBYTEN4.XMBYTEN4
---

# XMBYTEN4::XMBYTEN4(int8_t,int8_t,int8_t,int8_t)


## -description

Initializes a new instance of <code>XMBYTEN4</code> from four <code>int8_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/62d61a35-8674-4855-b09c-f351363cd50b">XMBYTEN4 
	</a> from a
	four <code>int8_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMBYTEN4</code> instance.

### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMBYTEN4</code> instance.

### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMBYTEN4</code> instance.

### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMBYTEN4</code> instance.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of
	    this constructor:
	


```

	    XMBYTEN4 instance;

	    instance.x = _x; 
	    instance.y = _y; 
	    instance.z = _z; 
	    instance.w = _w;

	
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>



<a href="/windows/desktop/dxmath/xmbyten4-ctor">XMBYTEN4 Constructors</a>