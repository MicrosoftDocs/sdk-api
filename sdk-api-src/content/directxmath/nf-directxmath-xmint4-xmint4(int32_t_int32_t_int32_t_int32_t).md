---
UID: NF:directxmath.XMINT4.XMINT4(int32_t,int32_t,int32_t,int32_t)
title: XMINT4::XMINT4(int32_t,int32_t,int32_t,int32_t) (directxmath.h)
description: Initializes a new instance of XMINT4 from four int32_t arguments.
helpviewer_keywords: ["XMINT4","XMINT4 constructor [DirectX Math Support APIs]","XMINT4 constructor [DirectX Math Support APIs]","XMINT4 structure","XMINT4 structure [DirectX Math Support APIs]","XMINT4 constructor","XMINT4.XMINT4","XMINT4.XMINT4(int32_t","int32_t","int32_t","int32_t)","XMINT4::XMINT4","XMINT4::XMINT4(int32_t","int32_t","int32_t","int32_t)","dxmath.xmint4_ctor_2"]
old-location: dxmath\xmint4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMINT4.#ctor(int32_t,int32_t,int32_t,int32_t)
ms.date: 12/05/2018
ms.keywords: XMINT4, XMINT4 constructor [DirectX Math Support APIs], XMINT4 constructor [DirectX Math Support APIs],XMINT4 structure, XMINT4 structure [DirectX Math Support APIs],XMINT4 constructor, XMINT4.XMINT4, XMINT4.XMINT4(int32_t,int32_t,int32_t,int32_t), XMINT4::XMINT4, XMINT4::XMINT4(int32_t,int32_t,int32_t,int32_t), dxmath.xmint4_ctor_2
f1_keywords:
- directxmath/XMINT4.XMINT4
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectXMath.h
api_name:
- XMINT4.XMINT4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMINT4::XMINT4(int32_t,int32_t,int32_t,int32_t)


## -description


Initializes a new instance of <code>XMINT4</code> from four <code>int32_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmint4">XMINT4</a> from four
	<code>int32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMINT4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMINT4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMINT4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMINT4</code> instance.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:
	


```

	XMINT4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmint4">XMINT4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmint4-xmint4(constint32_t)">XMINT4 Constructors</a>
 

 

