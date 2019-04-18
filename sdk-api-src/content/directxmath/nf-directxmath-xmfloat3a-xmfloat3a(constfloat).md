---
UID: NF:directxmath.XMFLOAT3A.XMFLOAT3A(const float)
title: XMFLOAT3A::XMFLOAT3A(const float) (directxmath.h)
author: windows-sdk-content
description: Initializes a new instance of XMFLOAT3 from a three element float array argument.
old-location: dxmath\xmfloat3_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT3.#ctor(const float)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XMFLOAT3 constructor [DirectX Math Support APIs], XMFLOAT3 constructor [DirectX Math Support APIs],XMFLOAT3 structure, XMFLOAT3 structure [DirectX Math Support APIs],XMFLOAT3 constructor, XMFLOAT3.XMFLOAT3(const float*), XMFLOAT3A, XMFLOAT3A.XMFLOAT3A, XMFLOAT3A.XMFLOAT3A(const float), XMFLOAT3A::XMFLOAT3A, XMFLOAT3A::XMFLOAT3A(const float), dxmath.xmfloat3_ctor_3
ms.topic: method
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
 - XMFLOAT3.XMFLOAT3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMFLOAT3A::XMFLOAT3A(const float)


## -description


Initializes a new instance of <code>XMFLOAT3</code> from a three element <code>float</code> array argument.

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419475(v=VS.85).aspx">XMFLOAT3</a> from a from a three element
  <code>float</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.</div><div> </div>

## -parameters




### -param pArray

Three element floating point array containing the values used to initialize the three components of a new instance of
        <code>XMFLOAT3</code>.


## -remarks



The following pseudocode demonstrates the operation of this constructor:


```

	XMFLOAT3 instance;
	instance.x =  pArray[0];
	instance.y =  pArray[1];
	instance.z =  pArray[2];
    
```





## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419475(v=VS.85).aspx">XMFLOAT3</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415292(v=VS.85).aspx">XMFLOAT3 Constructors</a>
 

 

