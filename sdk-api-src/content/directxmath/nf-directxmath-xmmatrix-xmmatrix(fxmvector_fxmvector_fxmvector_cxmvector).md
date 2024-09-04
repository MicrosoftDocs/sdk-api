---
UID: NF:directxmath.XMMATRIX.XMMATRIX(FXMVECTOR,FXMVECTOR,FXMVECTOR,CXMVECTOR)
title: XMMATRIX::XMMATRIX(FXMVECTOR,FXMVECTOR,FXMVECTOR,CXMVECTOR) (directxmath.h)
description: Initializes a new instance of the XMMATRIX structure from four instances of XMVECTOR.
helpviewer_keywords: ["XMMATRIX","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX structure","XMMATRIX structure [DirectX Math Support APIs]","XMMATRIX constructor","XMMATRIX.XMMATRIX","XMMATRIX.XMMATRIX()","XMMATRIX.XMMATRIX(FXMVECTOR","FXMVECTOR","FXMVECTOR","CXMVECTOR)","XMMATRIX::XMMATRIX","XMMATRIX::XMMATRIX(FXMVECTOR","FXMVECTOR","FXMVECTOR","CXMVECTOR)","dxmath.xmmatrix_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 8b405a17-be16-4001-b076-95acca0ce467
ms.date: 05/13/2019
ms.keywords: XMMATRIX, XMMATRIX constructor [DirectX Math Support APIs], XMMATRIX constructor [DirectX Math Support APIs],XMMATRIX structure, XMMATRIX structure [DirectX Math Support APIs],XMMATRIX constructor, XMMATRIX.XMMATRIX, XMMATRIX.XMMATRIX(), XMMATRIX.XMMATRIX(FXMVECTOR,FXMVECTOR,FXMVECTOR,CXMVECTOR), XMMATRIX::XMMATRIX, XMMATRIX::XMMATRIX(FXMVECTOR,FXMVECTOR,FXMVECTOR,CXMVECTOR), dxmath.xmmatrix_ctor_1
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
 - XMMATRIX::XMMATRIX
 - directxmath/XMMATRIX::XMMATRIX
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
 - XMMATRIX.XMMATRIX
---

# XMMATRIX::XMMATRIX(FXMVECTOR,FXMVECTOR,FXMVECTOR,CXMVECTOR)


## -description

Initializes a new instance of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> structure from four instances of <code>XMVECTOR</code>.

Initializes a new instance of the **XMMATRIX** structure from four instances of **XMVECTOR Data Type**.

<div class="alert"><b>Note</b>  This constructor is only available when developing with C++.</div>

## -parameters

### -param R0

Instance of **XMMATRIX** used to initialize the first row of a new instance of **XMMATRIX**.

### -param R1

Instance of **XMMATRIX** used to initialize the second row of a new instance of **XMMATRIX**.

### -param R2

Instance of **XMMATRIX** used to initialize the third row of a new instance of **XMMATRIX**.

### -param R3

Instance of **XMMATRIX** used to initialize the fourth row of a new instance of **XMMATRIX**.

## -remarks

The following two pseudocode examples demonstrate the operation of this constructor:

```cpp
XMMATRIX mat;
XMVECTOR rows[4];
//...Initialize instances of XMVECTOR
for (int i=0;i<4;i++){
    for (int j=0;j<4;j++){
        mat.m[i][j]=rows[i].v[j];
    }
}
```

Or

```cpp
XMMATRIX mat;
XMVECTOR rows[4];
//...Initialize instances of XMVECTOR
for (int i=0;i<4;i++){
    mat.r[i]=rows[i];
}
```

## -see-also

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>

<a href="/windows/desktop/dxmath/xmmatrix-ctor">XMMATRIX Constructors</a>