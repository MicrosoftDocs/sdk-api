---
UID: NF:directxmath.XMStoreInt4
title: XMStoreInt4 function (directxmath.h)
author: windows-sdk-content
description: Stores an XMVECTOR in a 4-element uint32_t array.
old-location: dxmath\xmstoreint4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreInt4(VOID@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMStoreInt4, XMStoreInt4, XMStoreInt4 method [DirectX Math Support APIs], dxmath.xmstoreint4
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
 - XMStoreInt4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMStoreInt4 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in a 4-element <b>uint32_t</b> array.


## -parameters




### -param pDestination [out]

Address at which to store the data.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



The following pseudocode shows you the operation of the function.


```
uint32_t* pElement = (uint32_t*)pDestination;

assert(pDestination);

pElement[0] = V.u[0];
pElement[1] = V.u[1];
pElement[2] = V.u[2];
pElement[3] = V.u[3];
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff728760(v=VS.85).aspx">XMINT4</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404703(v=VS.85).aspx">XMStoreSInt4</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404708(v=VS.85).aspx">XMStoreUInt4</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404755(v=VS.85).aspx">XMUINT4</a>
 

 

