---
UID: NF:directxpackedvector.XMUSHORT2.XMUSHORT2(float,float)
title: XMUSHORT2::XMUSHORT2(float,float) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORT2 from two float arguments.
helpviewer_keywords: ["XMUSHORT2","XMUSHORT2 constructor [DirectX Math Support APIs]","XMUSHORT2 constructor [DirectX Math Support APIs]","XMUSHORT2 structure","XMUSHORT2 structure [DirectX Math Support APIs]","XMUSHORT2 constructor","XMUSHORT2.XMUSHORT2","XMUSHORT2.XMUSHORT2(float","float)","XMUSHORT2::XMUSHORT2","XMUSHORT2::XMUSHORT2(float","float)","dxmath.xmushort2_ctor_4"]
old-location: dxmath\xmushort2_ctor_4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUSHORT2.#ctor(float,float)
ms.date: 12/05/2018
ms.keywords: XMUSHORT2, XMUSHORT2 constructor [DirectX Math Support APIs], XMUSHORT2 constructor [DirectX Math Support APIs],XMUSHORT2 structure, XMUSHORT2 structure [DirectX Math Support APIs],XMUSHORT2 constructor, XMUSHORT2.XMUSHORT2, XMUSHORT2.XMUSHORT2(float,float), XMUSHORT2::XMUSHORT2, XMUSHORT2::XMUSHORT2(float,float), dxmath.xmushort2_ctor_4
f1_keywords:
- directxpackedvector/XMUSHORT2.XMUSHORT2
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
req.namespace: Use DirectX.
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
- directxpackedvector.h
api_name:
- XMUSHORT2.XMUSHORT2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUSHORT2::XMUSHORT2(float,float)


## -description


Initializes a new instance of <code>XMUSHORT2</code> from two <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a> from two
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUSHORT2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUSHORT2</code> instance.
		


## -remarks



The magnitude of each argument to the constructor will be clamped to the range supported
	    by an 16-bit unsigned integer [0.0, 65535.0].
	

The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUSHORT2 instance;

	instance.x = (uint16_t)min( max( _x, 0.0 ), 65535.0 );
	instance.y = (uint16_t)min( max( _y, 0.0 ), 65535.0 );
    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a>



<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmushort2-ctor">XMUSHORT2 Constructors</a>
 

 

