---
UID: NF:directxmath.XMFLOAT2.XMFLOAT2(constfloat)
title: XMFLOAT2::XMFLOAT2(const float) (directxmath.h)
description: Initializes a new instance of XMFLOAT2 from a two element float array argument.
helpviewer_keywords: ["XMFLOAT2","XMFLOAT2 constructor [DirectX Math Support APIs]","XMFLOAT2 constructor [DirectX Math Support APIs]","XMFLOAT2 structure","XMFLOAT2 structure [DirectX Math Support APIs]","XMFLOAT2 constructor","XMFLOAT2.XMFLOAT2","XMFLOAT2.XMFLOAT2(const float)","XMFLOAT2.XMFLOAT2(const float*)","XMFLOAT2::XMFLOAT2","XMFLOAT2::XMFLOAT2(const float)","dxmath.xmfloat2_ctor_3"]
old-location: dxmath\xmfloat2_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT2.#ctor(const float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT2, XMFLOAT2 constructor [DirectX Math Support APIs], XMFLOAT2 constructor [DirectX Math Support APIs],XMFLOAT2 structure, XMFLOAT2 structure [DirectX Math Support APIs],XMFLOAT2 constructor, XMFLOAT2.XMFLOAT2, XMFLOAT2.XMFLOAT2(const float), XMFLOAT2.XMFLOAT2(const float*), XMFLOAT2::XMFLOAT2, XMFLOAT2::XMFLOAT2(const float), dxmath.xmfloat2_ctor_3
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
 - XMFLOAT2::XMFLOAT2
 - directxmath/XMFLOAT2::XMFLOAT2
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
 - XMFLOAT2.XMFLOAT2
---

# XMFLOAT2::XMFLOAT2(const float)


## -description

Initializes a new instance of <code>XMFLOAT2</code> from a two element <code>float</code> array
	argument.
    

This constructor initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a> from a from
	a two element <code>float</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters

### -param pArray

Two element <code>float</code> array containing the values used to initialize the
		    two components of a new instance of <code>XMFLOAT2</code>.

## -remarks

```

	XMFLOAT2 instance;
	instance.x = pArray[0];
	instance.y = pArray[1];
	instance.z = pArray[2];
	instance.w = pArray[3];

    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2">XMFLOAT2</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmfloat2-xmfloat2(constfloat)">XMFLOAT2 Constructors</a>