---
UID: NF:directxmath.XMINT3.XMINT3(int32_t,int32_t,int32_t)
title: XMINT3::XMINT3(int32_t,int32_t,int32_t) (directxmath.h)
description: Initializes a new instance of XMINT3 from three int32_t arguments.
helpviewer_keywords: ["XMINT3","XMINT3 constructor [DirectX Math Support APIs]","XMINT3 constructor [DirectX Math Support APIs]","XMINT3 structure","XMINT3 structure [DirectX Math Support APIs]","XMINT3 constructor","XMINT3.XMINT3","XMINT3.XMINT3(int32_t","int32_t","int32_t)","XMINT3::XMINT3","XMINT3::XMINT3(int32_t","int32_t","int32_t)","dxmath.xmint3_ctor_2"]
old-location: dxmath\xmint3_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMINT3.#ctor(int32_t,int32_t,int32_t)
ms.date: 12/05/2018
ms.keywords: XMINT3, XMINT3 constructor [DirectX Math Support APIs], XMINT3 constructor [DirectX Math Support APIs],XMINT3 structure, XMINT3 structure [DirectX Math Support APIs],XMINT3 constructor, XMINT3.XMINT3, XMINT3.XMINT3(int32_t,int32_t,int32_t), XMINT3::XMINT3, XMINT3::XMINT3(int32_t,int32_t,int32_t), dxmath.xmint3_ctor_2
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
 - XMINT3::XMINT3
 - directxmath/XMINT3::XMINT3
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
 - XMINT3.XMINT3
---

# XMINT3::XMINT3(int32_t,int32_t,int32_t)


## -description

Initializes a new instance of <code>XMINT3</code> from three <code>int32_t</code> arguments.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a> from three <code>int32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param _x

Value to be stored in the x-component (the <b>x</b> member) of the new instance of
	    <code>XMINT3</code>.

### -param _y

Value to be stored in the y-component (the <b>y</b> member) of the new instance of
	    <code>XMINT3</code>.

### -param _z

Value to be stored in the z-component (the <b>z</b> member) of the new instance of
	    <code>XMINT3</code>.

## -remarks

The following pseudocode demonstrates the operation of this constructor:


```

	XMINT3 instance;
	instance.x =  _x;
	instance.y =  _y;
	instance.z =  _z;
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmint3-xmint3(constint32_t)">XMINT3 Constructors</a>