---
UID: NF:directxpackedvector.XMBYTE2.XMBYTE2(float,float)
title: XMBYTE2::XMBYTE2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTE2 from two float arguments.
helpviewer_keywords: ["XMBYTE2","XMBYTE2 constructor [DirectX Math Support APIs]","XMBYTE2 constructor [DirectX Math Support APIs]","XMBYTE2 structure","XMBYTE2 structure [DirectX Math Support APIs]","XMBYTE2 constructor","XMBYTE2.XMBYTE2","XMBYTE2.XMBYTE2(float","float)","XMBYTE2::XMBYTE2","XMBYTE2::XMBYTE2(float","float)","dxmath.xmbyte2_ctor_4"]
old-location: dxmath\xmbyte2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMBYTE2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMBYTE2, XMBYTE2 constructor [DirectX Math Support APIs], XMBYTE2 constructor [DirectX Math Support APIs],XMBYTE2 structure, XMBYTE2 structure [DirectX Math Support APIs],XMBYTE2 constructor, XMBYTE2.XMBYTE2, XMBYTE2.XMBYTE2(float,float), XMBYTE2::XMBYTE2, XMBYTE2::XMBYTE2(float,float), dxmath.xmbyte2_ctor_4
f1_keywords:
- directxpackedvector/XMBYTE2.XMBYTE2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXPackedVector.h
api_name:
- XMBYTE2.XMBYTE2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMBYTE2::XMBYTE2(float,float)


## -description


Initializes a new instance of <code>XMBYTE2</code> from two <code>float</code> arguments.

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a> from two <code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available with C++.</div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new <code>XMBYTE2</code> instance.


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new <code>XMBYTE2</code> instance.


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported by an 8-bit signed integer
   [-127.0, 127.0].

The following pseudocode demonstrates the operation of this constructor:


```

	XMBYTE2 instance;

	instance.x = (int8_t)min( max( _x, -127.0 ), 127.0 );
	instance.y = (int8_t)min( max( _y, -127.0 ), 127.0 );
    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmbyte2-ctor">XMBYTE2 Constructors</a>
 

 

