---
UID: NF:directxmath.XMFLOAT4A.XMFLOAT4A(constfloat)
title: XMFLOAT4A::XMFLOAT4A(const float) (directxmath.h)
description: Initializes a new instance of XMFLOAT4 from a four element float array argument.
helpviewer_keywords: ["XMFLOAT4 constructor [DirectX Math Support APIs]","XMFLOAT4 constructor [DirectX Math Support APIs]","XMFLOAT4 structure","XMFLOAT4 structure [DirectX Math Support APIs]","XMFLOAT4 constructor","XMFLOAT4.XMFLOAT4(const float*)","XMFLOAT4A","XMFLOAT4A.XMFLOAT4A","XMFLOAT4A.XMFLOAT4A(const float)","XMFLOAT4A::XMFLOAT4A","XMFLOAT4A::XMFLOAT4A(const float)","dxmath.xmfloat4_ctor_3"]
old-location: dxmath\xmfloat4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT4.#ctor(const float)
ms.date: 12/05/2018
ms.keywords: XMFLOAT4 constructor [DirectX Math Support APIs], XMFLOAT4 constructor [DirectX Math Support APIs],XMFLOAT4 structure, XMFLOAT4 structure [DirectX Math Support APIs],XMFLOAT4 constructor, XMFLOAT4.XMFLOAT4(const float*), XMFLOAT4A, XMFLOAT4A.XMFLOAT4A, XMFLOAT4A.XMFLOAT4A(const float), XMFLOAT4A::XMFLOAT4A, XMFLOAT4A::XMFLOAT4A(const float), dxmath.xmfloat4_ctor_3
f1_keywords:
- directxmath/XMFLOAT4.XMFLOAT4
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
- XMFLOAT4.XMFLOAT4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT4A::XMFLOAT4A(const float)


## -description


Initializes a new instance of <code>XMFLOAT4</code> from a four element <code>float</code> array
	argument.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat4">XMFLOAT4</a> from a from
	a four element <code>float</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param pArray

Four element <code>float</code> array containing the values used to initialize the
		    four components of a new instance of <code>XMFLOAT4</code>.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:


```

	XMFLOAT4 instance;
	instance.x = pArray[0];
	instance.y = pArray[1];
	instance.z = pArray[2];
	instance.w = pArray[3];

    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/ns-directxmath-xmfloat4">XMFLOAT4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmfloat4-xmfloat4(constfloat)">XMFLOAT4 Constructors</a>
 

 

