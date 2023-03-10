---
UID: NF:directxmath.XMMATRIX.XMMATRIX(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)
title: XMMATRIX::XMMATRIX(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float) (directxmath.h)
description: Initializes a new instance of the XMMATRIX structure from sixteen scalar float values.
helpviewer_keywords: ["XMMATRIX","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX constructor [DirectX Math Support APIs]","XMMATRIX structure","XMMATRIX structure [DirectX Math Support APIs]","XMMATRIX constructor","XMMATRIX.XMMATRIX","XMMATRIX.XMMATRIX(float","float","float","float","float","float","float","float","float","float","float","float","float","float","float","float)","XMMATRIX::XMMATRIX","XMMATRIX::XMMATRIX(float","float","float","float","float","float","float","float","float","float","float","float","float","float","float","float)","dxmath.xmmatrix_ctor_2"]
old-location: dxmath\xmmatrix_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMMATRIX.#ctor(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMMATRIX, XMMATRIX constructor [DirectX Math Support APIs], XMMATRIX constructor [DirectX Math Support APIs],XMMATRIX structure, XMMATRIX structure [DirectX Math Support APIs],XMMATRIX constructor, XMMATRIX.XMMATRIX, XMMATRIX.XMMATRIX(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float), XMMATRIX::XMMATRIX, XMMATRIX::XMMATRIX(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float), dxmath.xmmatrix_ctor_2
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

# XMMATRIX::XMMATRIX(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)


## -description

Initializes a new instance of the <code>XMMATRIX</code> structure from sixteen scalar
	<code>float</code> values.
    

Initializes a new instance of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a> structure from sixteen
	scalar <code>float</code> values.
<div class="alert"><b>Note</b>  This constructor is only available when developing with C++.
    </div><div> </div>

## -parameters

### -param m00

Value used to initialize the <b>_11</b> member of the <code>XMMATRIX</code> structure.

### -param m01

Value used to initialize the <b>_12</b> member of the <code>XMMATRIX</code> structure.

### -param m02

Value used to initialize the <b>_13</b> member of the <code>XMMATRIX</code> structure.

### -param m03

Value used to initialize the <b>_14</b> member of the <code>XMMATRIX</code> structure.

### -param m10

Value used to initialize the <b>_21</b> member of the <code>XMMATRIX</code> structure.

### -param m11

Value used to initialize the <b>_22</b> member of the <code>XMMATRIX</code> structure.

### -param m12

Value used to initialize the <b>_23</b> member of the <code>XMMATRIX</code> structure.

### -param m13

Value used to initialize the <b>_24</b> member of the <code>XMMATRIX</code> structure.

### -param m20

Value used to initialize the <b>_31</b> member of the <code>XMMATRIX</code> structure.

### -param m21

Value used to initialize the <b>_32</b> member of the <code>XMMATRIX</code> structure.

### -param m22

Value used to initialize the <b>_33</b> member of the <code>XMMATRIX</code> structure.

### -param m23

Value used to initialize the <b>_34</b> member of the <code>XMMATRIX</code> structure.

### -param m30

Value used to initialize the <b>_41</b> member of the <code>XMMATRIX</code> structure.

### -param m31

Value used to initialize the <b>_42</b> member of the <code>XMMATRIX</code> structure.

### -param m32

Value used to initialize the <b>_43</b> member of the <code>XMMATRIX</code> structure.

### -param m33

Value used to initialize the <b>_44</b> member of the <code>XMMATRIX</code> structure.

## -remarks

The following pseudocode example demonstrates the operation of this constructor:
	


```

   XMMATRIX mat;
   mat._11 = m00;
   mat._12 = m01;
   mat._13 = m02;
   mat._14 = m03;
   mat._21 = m10;
   mat._22 = m11;
   mat._23 = m12;
   mat._24 = m13;
   mat._31 = m20;
   mat._32 = m21;
   mat._33 = m22;
   mat._34 = m23;
   mat._41 = m30;
   mat._42 = m31;
   mat._43 = m32;
   mat._44 = m33;
      
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix">XMMATRIX</a>



<a href="/windows/desktop/dxmath/xmmatrix-ctor">XMMATRIX Constructors</a>