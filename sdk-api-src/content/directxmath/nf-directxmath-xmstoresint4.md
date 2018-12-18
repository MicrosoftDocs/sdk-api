---
UID: NF:directxmath.XMStoreSInt4
title: XMStoreSInt4 function
author: windows-sdk-content
description: Stores signed integer data from an XMVECTOR in an XMINT4 structure.
old-location: dxmath\xmstoresint4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreSInt4(XMINT4@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMStoreSInt4, XMStoreSInt4, XMStoreSInt4 method [DirectX Math Support APIs], dxmath.xmstoresint4
ms.topic: function
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
 - XMStoreSInt4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreSInt4 function


## -description


Stores signed integer data from an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <b>XMINT4</b> structure.


## -parameters




### -param pDestination [out]

Address of an  <a href="https://msdn.microsoft.com/en-us/library/Ff728760(v=VS.85).aspx">XMINT4</a> structure in which to store the data.


### -param V

Vector containing the data to store.


## -returns



None.




## -remarks



For 16-byte aligned memory, it may be faster to use <a href="https://msdn.microsoft.com/en-us/library/Ee420366(v=VS.85).aspx">XMStoreInt4A</a> 
    with a casting operator.

The following pseudocode shows the operation of this function.


```

XMVECTOR N;	

assert(pDestination);

N = XMVectorClamp(V, MinInt, MaxInt );
N = XMVectorRound(N);

pDestination->x = (int32_t)N.v[0];
pDestination->y = (int32_t)N.v[1];
pDestination->z = (int32_t)N.v[2];
pDestination->w = (int32_t)N.v[3];

    
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

