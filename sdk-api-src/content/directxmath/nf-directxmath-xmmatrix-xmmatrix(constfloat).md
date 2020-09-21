---
UID: NF:directxmath.XMMATRIX.XMMATRIX(constfloat)
title: XMMATRIX::XMMATRIX(const float) (directxmath.h)
description: Initializes a new instance of the XMMATRIX structure from a sixteen element float array.
helpviewer_keywords: ["XMMATRIX","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX structure","XMMATRIX structure [DirectX Math Support APIs]","XMMATRIX constructor","XMMATRIX.XMMATRIX","XMMATRIX.XMMATRIX()","XMMATRIX.XMMATRIX(const float)","XMMATRIX::XMMATRIX","XMMATRIX::XMMATRIX(const float)","dxmath.xmmatrix_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 1c778c4c-03eb-4632-b7d4-c1e3caa61368
ms.date: 05/13/2019
ms.keywords: XMMATRIX, XMMATRIX constructor [DirectX Math Support APIs], XMMATRIX constructor [DirectX Math Support APIs],XMMATRIX structure, XMMATRIX structure [DirectX Math Support APIs],XMMATRIX constructor, XMMATRIX.XMMATRIX, XMMATRIX.XMMATRIX(), XMMATRIX.XMMATRIX(const float), XMMATRIX::XMMATRIX, XMMATRIX::XMMATRIX(const float), dxmath.xmmatrix_ctor_1
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

# XMMATRIX::XMMATRIX(const float)


## -description

Initializes a new instance of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> structure from a sixteen element <code>float</code> array.

Initializes a new instance of the **XMMATRIX** structure from a sixteen element <code>float</code> array.

<div class="alert"><b>Note</b>  This constructor is only available when developing with C++.</div><div> </div>

## -parameters

### -param pArray

Address of a 16 element <wdcml:mark type="appdef" xmlns:wdcml="http://microsoft.com/wdcml">float</wdcml:mark> array, specifying the value of each member of a new instance of **XMMATRIX**.

## -remarks

The matrix elements are stored in *pArray* in *row-major* order.

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMMATRIX mat;
mat._11=pArray[0];
mat._12=pArray[1];
mat._13=pArray[2];
mat._14=pArray[3];
mat._21=pArray[4];
mat._22=pArray[5];
mat._23=pArray[6];
mat._24=pArray[7];
mat._31=pArray[8];
mat._32=pArray[9];
mat._33=pArray[10];
mat._34=pArray[11];
mat._41=pArray[12];
mat._42=pArray[13];
mat._43=pArray[14];
mat._44=pArray[15];
```

## -see-also

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>

<a href="/windows/desktop/dxmath/xmmatrix-ctor">XMMATRIX Constructors</a>