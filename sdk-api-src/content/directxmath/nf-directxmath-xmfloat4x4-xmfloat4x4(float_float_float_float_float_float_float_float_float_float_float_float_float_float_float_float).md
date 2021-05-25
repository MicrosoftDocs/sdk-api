---
UID: NF:directxmath.XMFLOAT4X4.XMFLOAT4X4(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)
title: XMFLOAT4X4::XMFLOAT4X4(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float) (directxmath.h)
description: Initializes a new instance of the XMFLOAT4X4 structure from sixteen scalar float values.
helpviewer_keywords: ["XMFLOAT4X4","XMFLOAT4X4 constructor [DirectX Math Support APIs]","XMFLOAT4X4 constructor [DirectX Math Support APIs]","XMFLOAT4X4 structure","XMFLOAT4X4 structure [DirectX Math Support APIs]","XMFLOAT4X4 constructor","XMFLOAT4X4.XMFLOAT4X4","XMFLOAT4X4.XMFLOAT4X4(float","float","float","float","float","float","float","float","float","float","float","float","float","float","float","float)","XMFLOAT4X4::XMFLOAT4X4","XMFLOAT4X4::XMFLOAT4X4(float","float","float","float","float","float","float","float","float","float","float","float","float","float","float","float)","dxmath.xmfloat4x4_ctor_2"]
old-location: dxmath\xmfloat4x4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT4X4.#ctor(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT4X4, XMFLOAT4X4 constructor [DirectX Math Support APIs], XMFLOAT4X4 constructor [DirectX Math Support APIs],XMFLOAT4X4 structure, XMFLOAT4X4 structure [DirectX Math Support APIs],XMFLOAT4X4 constructor, XMFLOAT4X4.XMFLOAT4X4, XMFLOAT4X4.XMFLOAT4X4(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float), XMFLOAT4X4::XMFLOAT4X4, XMFLOAT4X4::XMFLOAT4X4(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float), dxmath.xmfloat4x4_ctor_2
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
 - XMFLOAT4X4::XMFLOAT4X4
 - directxmath/XMFLOAT4X4::XMFLOAT4X4
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
 - XMFLOAT4X4.XMFLOAT4X4
---

# XMFLOAT4X4::XMFLOAT4X4(float,float,float,float,float,float,float,float,float,float,float,float,float,float,float,float)


## -description

Initializes a new instance of the <code>XMFLOAT4X4</code> structure from sixteen scalar
	<code>float</code> values.
    

Initializes a new instance of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a> structure from sixteen
	scalar <code>float</code> values.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param m00

Value used to initialize the <b>_11</b> member (equivalently the <b>m[0,0]</b> member) of the <code>XMFLOAT4X4</code> structure.

### -param m01

Value used to initialize the <b>_12</b> member (equivalently the
		<b>m[0,1]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m02

Value used to initialize the <b>_13</b> member (equivalently the
		<b>m[0,2]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m03

Value used to initialize the <b>_14</b> member (equivalently the
		<b>m[0,3]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m10

Value used to initialize the <b>_21</b> member (equivalently the
		<b>m[1,0]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m11

Value used to initialize the <b>_22</b> member (equivalently the
		<b>m[1,1]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m12

Value used to initialize the <b>_23</b> member (equivalently the
		<b>m[1,2]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m13

Value used to initialize the <b>_24</b> member (equivalently the
		<b>m[1,3]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m20

Value used to initialize the <b>_31</b> member (equivalently the
		<b>m[2,0]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m21

Value used to initialize the <b>_32</b> member (equivalently the
		<b>m[2,1]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m22

Value used to initialize the <b>_33</b> member (equivalently the
		<b>m[2,2]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m23

Value used to initialize the <b>_34</b> member (equivalently the
		<b>m[2,3]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m30

Value used to initialize the <b>_41</b> member (equivalently the
		<b>m[3,0]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m31

Value used to initialize the <b>_42</b> member (equivalently the
		<b>m[3,1]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m32

Value used to initialize the <b>_43</b> member (equivalently the
		<b>m[3,2]</b>) of the <code>XMFLOAT4X4</code> structure.

### -param m33

Value used to initialize the <b>_34</b> member (equivalently the
		<b>m[3,3]</b>) of the <code>XMFLOAT4X4</code> structure.

## -remarks

The following two pseudocode examples demonstrate the operation of this constructor:
	


```

   XMFLOAT4X4 mat;
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


Or
      


```

   XMFLOAT4X4 mat;
   mat.m[0,0] = m00;
   mat.m[0,1] = m01;
   mat.m[0,2] = m02;
   mat.m[0,3] = m03;
   mat.m[1,0] = m10;
   mat.m[1,1] = m11;
   mat.m[1,2] = m12;
   mat.m[1,3] = m13;
   mat.m[2,0] = m20;
   mat.m[2,1] = m21;
   mat.m[2,2] = m22;
   mat.m[2,3] = m23;
   mat.m[3,0] = m30;
   mat.m[3,1] = m31;
   mat.m[3,2] = m32;
   mat.m[3,3] = m33;
     
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4">XMFLOAT4X4</a>



<a href="/windows/desktop/dxmath/xmfloat4x4-ctor">XMFLOAT4X4 Constructors</a>