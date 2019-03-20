---
UID: NF:directxmath.XMFLOAT4.XMFLOAT4(float,float,float,float)
title: XMFLOAT4::XMFLOAT4(float,float,float,float) (directxmath.h)
author: windows-sdk-content
description: Initializes a new instance of XMFLOAT4 from four float arguments.
old-location: dxmath\xmfloat4_ctor_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMFLOAT4.#ctor(float,float,float,float)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: XMFLOAT4, XMFLOAT4 constructor [DirectX Math Support APIs], XMFLOAT4 constructor [DirectX Math Support APIs],XMFLOAT4 structure, XMFLOAT4 structure [DirectX Math Support APIs],XMFLOAT4 constructor, XMFLOAT4.XMFLOAT4, XMFLOAT4.XMFLOAT4(float,float,float,float), XMFLOAT4::XMFLOAT4, XMFLOAT4::XMFLOAT4(float,float,float,float), dxmath.xmfloat4_ctor_2
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
 - XMFLOAT4.XMFLOAT4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMFLOAT4::XMFLOAT4(float,float,float,float)


## -description


Initializes a new instance of <code>XMFLOAT4</code> from four <code>float</code> arguments.
    

This constructor initializes a new instance of <a href="https://msdn.microsoft.com/en-us/library/Ee419608(v=VS.85).aspx">XMFLOAT4</a> from four
	<code>float</code> arguments.
<div class="alert"><b>Note</b>  This constructor is only available under C++.
    </div><div> </div>

## -parameters




### -param _x

Value of the x-coordinate of the vector, the <b>x</b> member of the new
		    <code>XMFLOAT4</code> instance.
		


### -param _y

Value of the y-coordinate of the vector, the <b>y</b> member of the new
		    <code>XMFLOAT4</code> instance.
		


### -param _z

Value of the z-coordinate of the vector, the <b>z</b> member of the new
		    <code>XMFLOAT4</code> instance.
		


### -param _w

Value of the w-coordinate of the vector, the <b>w</b> member of the new
		    <code>XMFLOAT4</code> instance.
		


## -remarks



The following pseudocode demonstrates the operation of this constructor:
	


```

	XMFLOAT4 instance;

	instance.x = _x;
	instance.y = _y;
	instance.z = _z;
	instance.w = _w;

    
```





## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Ee419608(v=VS.85).aspx">XMFLOAT4</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415309(v=VS.85).aspx">XMFLOAT4 Constructors</a>
 

 

