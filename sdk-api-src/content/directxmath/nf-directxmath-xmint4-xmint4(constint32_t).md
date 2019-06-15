---
UID: NF:directxmath.XMINT4.XMINT4(const int32_t)
title: XMINT4::XMINT4(const int32_t) (directxmath.h)
author: windows-sdk-content
description: Initializes a new instance of XMINT4 from a four element int32_t array argument.
old-location: dxmath\xmint4_ctor_3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMINT4.#ctor(const int32_t)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XMINT4, XMINT4 constructor [DirectX Math Support APIs], XMINT4 constructor [DirectX Math Support APIs],XMINT4 structure, XMINT4 structure [DirectX Math Support APIs],XMINT4 constructor, XMINT4.XMINT4, XMINT4.XMINT4(const int32_t), XMINT4.XMINT4(const int32_t*), XMINT4::XMINT4, XMINT4::XMINT4(const int32_t), dxmath.xmint4_ctor_3
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
 - XMINT4.XMINT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMINT4::XMINT4(const int32_t)


## -description


Initializes a new instance of <code>XMINT4</code> from a four element <code>int32_t</code> array
	argument.
    

This constructor initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmint4">XMINT4</a> from a from
	a four element <code>int32_t</code> array argument.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param pArray

Four element <code>int32_t</code> array containing the values used to initialize the
		    four components of a new instance of <code>XMINT4</code>.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:


```

	XMINT4 instance;
	instance.x = pArray[0];
	instance.y = pArray[1];
	instance.z = pArray[2];
	instance.w = pArray[3];

    
```





## -see-also




<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/xmint4">XMINT4</a>



<a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmint4-xmint4(constint32_t)">XMINT4 Constructors</a>
 

 

