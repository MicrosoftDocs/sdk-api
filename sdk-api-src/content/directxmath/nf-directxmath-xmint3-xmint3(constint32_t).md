---
UID: NF:directxmath.XMINT3.XMINT3(constint32_t)
title: XMINT3::XMINT3(const int32_t) (directxmath.h)
description: Initializes a new instance of XMINT3 from a three element int32_t array argument.
helpviewer_keywords: ["XMINT3","XMINT3 constructor [DirectX Math Support APIs]","XMINT3 constructor [DirectX Math Support APIs]","XMINT3 structure","XMINT3 structure [DirectX Math Support APIs]","XMINT3 constructor","XMINT3.XMINT3","XMINT3.XMINT3(const int32_t)","XMINT3.XMINT3(const int32_t*)","XMINT3::XMINT3","XMINT3::XMINT3(const int32_t)","dxmath.xmint3_ctor_3"]
old-location: dxmath\xmint3_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMINT3.#ctor(const int32_t)
ms.date: 12/05/2018
ms.keywords: XMINT3, XMINT3 constructor [DirectX Math Support APIs], XMINT3 constructor [DirectX Math Support APIs],XMINT3 structure, XMINT3 structure [DirectX Math Support APIs],XMINT3 constructor, XMINT3.XMINT3, XMINT3.XMINT3(const int32_t), XMINT3.XMINT3(const int32_t*), XMINT3::XMINT3, XMINT3::XMINT3(const int32_t), dxmath.xmint3_ctor_3
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

# XMINT3::XMINT3(const int32_t)


## -description

Initializes a new instance of <code>XMINT3</code> from a three element <code>int32_t</code> array argument.

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a> from a from a three element
  <code>int32_t</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param pArray

Three element <code>int32_t</code> array containing the values used to initialize the three components of a new instance of
        <code>XMINT3</code>.

## -remarks

The following pseudocode demonstrates the operation of this constructor:


```

	XMINT3 instance;
	instance.x =  pArray[0];
	instance.y =  pArray[1];
	instance.z =  pArray[2];
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmint3">XMINT3</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmint3-xmint3(constint32_t)">XMINT3 Constructors</a>