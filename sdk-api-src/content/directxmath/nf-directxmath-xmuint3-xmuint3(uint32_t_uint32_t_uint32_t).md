---
UID: NF:directxmath.XMUINT3.XMUINT3(uint32_t,uint32_t,uint32_t)
title: XMUINT3::XMUINT3(uint32_t,uint32_t,uint32_t) (directxmath.h)
description: Initializes a new instance of XMUINT3 from three uint32_t arguments.
helpviewer_keywords: ["XMUINT3","XMUINT3 constructor [DirectX Math Support APIs]","XMUINT3 constructor [DirectX Math Support APIs]","XMUINT3 structure","XMUINT3 structure [DirectX Math Support APIs]","XMUINT3 constructor","XMUINT3.XMUINT3","XMUINT3.XMUINT3(uint32_t","uint32_t","uint32_t)","XMUINT3::XMUINT3","XMUINT3::XMUINT3(uint32_t","uint32_t","uint32_t)","dxmath.xmuint3_ctor_2"]
old-location: dxmath\xmuint3_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUINT3.#ctor(uint32_t,uint32_t,uint32_t)
ms.date: 12/05/2018
ms.keywords: XMUINT3, XMUINT3 constructor [DirectX Math Support APIs], XMUINT3 constructor [DirectX Math Support APIs],XMUINT3 structure, XMUINT3 structure [DirectX Math Support APIs],XMUINT3 constructor, XMUINT3.XMUINT3, XMUINT3.XMUINT3(uint32_t,uint32_t,uint32_t), XMUINT3::XMUINT3, XMUINT3::XMUINT3(uint32_t,uint32_t,uint32_t), dxmath.xmuint3_ctor_2
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
 - XMUINT3::XMUINT3
 - directxmath/XMUINT3::XMUINT3
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
 - XMUINT3.XMUINT3
---

# XMUINT3::XMUINT3(uint32_t,uint32_t,uint32_t)


## -description

Initializes a new instance of <code>XMUINT3</code> from three <code>uint32_t</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint3">XMUINT3</a> from three <code>uint32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param _x

Value to be stored in the x-component (the <b>x</b> member) of the new instance of
	    <code>XMUINT3</code>.

### -param _y

Value to be stored in the y-component (the <b>y</b> member) of the new instance of
	    <code>XMUINT3</code>.

### -param _z

Value to be stored in the z-component (the <b>z</b> member) of the new instance of
	    <code>XMUINT3</code>.

## -remarks

The following pseudocode demonstrates the operation of this constructor:


```

	XMUINT3 instance;
	instance.x =  _x;
	instance.y =  _y;
	instance.z =  _z;
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint3">XMUINT3</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmuint3-xmuint3(constuint32_t)">XMUINT3 Constructors</a>