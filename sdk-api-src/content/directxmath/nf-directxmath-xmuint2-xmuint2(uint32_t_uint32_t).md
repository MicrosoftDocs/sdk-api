---
UID: NF:directxmath.XMUINT2.XMUINT2(uint32_t,uint32_t)
title: XMUINT2::XMUINT2(uint32_t,uint32_t) (directxmath.h)
author: windows-sdk-content
description: Initializes a new instance of XMUINT2 from two uint32_t arguments.
old-location: dxmath\xmuint2_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMUINT2.#ctor(uint32_t,uint32_t)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XMUINT2, XMUINT2 constructor [DirectX Math Support APIs], XMUINT2 constructor [DirectX Math Support APIs],XMUINT2 structure, XMUINT2 structure [DirectX Math Support APIs],XMUINT2 constructor, XMUINT2.XMUINT2, XMUINT2.XMUINT2(uint32_t,uint32_t), XMUINT2::XMUINT2, XMUINT2::XMUINT2(uint32_t,uint32_t), dxmath.xmuint2_ctor_2
ms.topic: method
f1_keywords: 
 - "directxmath/XMUINT2.XMUINT2"
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
 - XMUINT2.XMUINT2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUINT2::XMUINT2(uint32_t,uint32_t)


## -description


Initializes a new instance of <code>XMUINT2</code> from two <code>uint32_t</code> arguments.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmuint2">XMUINT2</a> from two
	<code>uint32_t</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMUINT2</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMUINT2</code> instance.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:
	


```

	XMUINT2 instance;

	instance.x = _x;
	instance.y = _y;

    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmuint2">XMUINT2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmuint2-xmuint2(constuint32_t)">XMUINT2 Constructors</a>
 

 

