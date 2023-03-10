---
UID: NF:directxmath.XMFLOAT3X3.XMFLOAT3X3(constfloat)
title: XMFLOAT3X3::XMFLOAT3X3(const float) (directxmath.h)
description: Initializes a new instance of the XMFLOAT3X3 structure from a nine element float array.
helpviewer_keywords: ["XMFLOAT3X3","XMFLOAT3X3 constructor [DirectX Math Support APIs]","XMFLOAT3X3 constructor [DirectX Math Support APIs]","XMFLOAT3X3 structure","XMFLOAT3X3 structure [DirectX Math Support APIs]","XMFLOAT3X3 constructor","XMFLOAT3X3.XMFLOAT3X3","XMFLOAT3X3.XMFLOAT3X3(const float)","XMFLOAT3X3.XMFLOAT3X3(const float*)","XMFLOAT3X3::XMFLOAT3X3","XMFLOAT3X3::XMFLOAT3X3(const float)","dxmath.xmfloat3x3_ctor_3"]
old-location: dxmath\xmfloat3x3_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3X3.#ctor(const float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT3X3, XMFLOAT3X3 constructor [DirectX Math Support APIs], XMFLOAT3X3 constructor [DirectX Math Support APIs],XMFLOAT3X3 structure, XMFLOAT3X3 structure [DirectX Math Support APIs],XMFLOAT3X3 constructor, XMFLOAT3X3.XMFLOAT3X3, XMFLOAT3X3.XMFLOAT3X3(const float), XMFLOAT3X3.XMFLOAT3X3(const float*), XMFLOAT3X3::XMFLOAT3X3, XMFLOAT3X3::XMFLOAT3X3(const float), dxmath.xmfloat3x3_ctor_3
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
 - XMFLOAT3X3::XMFLOAT3X3
 - directxmath/XMFLOAT3X3::XMFLOAT3X3
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
 - XMFLOAT3X3.XMFLOAT3X3
---

# XMFLOAT3X3::XMFLOAT3X3(const float)


## -description

Initializes a new instance of the <code>XMFLOAT3X3</code> structure from a nine element
	<code>float</code> array.
    

Initializes a new instance of the <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3x3">XMFLOAT3X3</a> structure from a nine
	element <code>float</code> array.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters

### -param pArray

Address of a 9 element <code>float</code> array, specifying the value of each member
		of a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3x3">XMFLOAT3X3</a>.

## -remarks

The matrix elements are stored in <b>pArray</b> in <i>row-major</i> order.

The following two pseudocode examples demonstrate the operation of this constructor:


```

   XMFLOAT3X3 mat;
   mat._11 = pArray[0];
   mat._12 = pArray[1];
   mat._13 = pArray[2];
   mat._21 = pArray[3];
   mat._22 = pArray[4];
   mat._23 = pArray[5];
   mat._31 = pArray[6];
   mat._32 = pArray[7];
   mat._33 = pArray[8];
    
```


Or


```

   XMFLOAT3X3 mat;
   mat.m[0,0] = pArray[0];
   mat.m[0,1] = pArray[1];
   mat.m[0,2] = pArray[2];
   mat.m[1,0] = pArray[3];
   mat.m[1,1] = pArray[4];
   mat.m[1,2] = pArray[5];
   mat.m[2,0] = pArray[6];
   mat.m[2,1] = pArray[7];
   mat.m[2,2] = pArray[8];
    
```

## -see-also

<b>Reference</b>



<a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3x3">XMFLOAT3X3</a>



<a href="/windows/desktop/dxmath/xmfloat3x3-ctor">XMFLOAT3X3 Constructors</a>