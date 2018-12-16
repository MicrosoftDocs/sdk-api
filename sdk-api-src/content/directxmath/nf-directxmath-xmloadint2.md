---
UID: NF:directxmath.XMLoadInt2
title: XMLoadInt2 function
author: windows-sdk-content
description: Loads data into the x and y components of an XMVECTOR.
old-location: dxmath\xmloadint2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt2(const uint32_t)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMLoadInt2, XMLoadInt2, XMLoadInt2 method [DirectX Math Support APIs], dxmath.xmloadint2
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
 - XMLoadInt2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadInt2 function


## -description


Loads data into the x and y components of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the data to load. 


## -returns



Returns an <code>XMVECTORI</code> loaded with the data from the <i>pSource</i>parameter.




## -remarks



The z and w components of the returned <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> will be initialized to 0.

For 16-byte aligned memory, it may be faster to use <a href="https://msdn.microsoft.com/2bf6c9d2-8440-4c2c-9fab-2af3885ccaa6">XMLoadInt2A</a> with a casting operator.

To convert the loaded <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> into float values, use <a href="https://msdn.microsoft.com/en-us/library/Hh437937(v=VS.85).aspx">XMConvertVectorUIntToFloat</a> or <a href="https://msdn.microsoft.com/en-us/library/Hh437934(v=VS.85).aspx">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = 0;
V.u[3] = 0;

return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404654(v=VS.85).aspx">XMINT2</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404675(v=VS.85).aspx">XMLoadSInt2</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404680(v=VS.85).aspx">XMLoadUInt2</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff728761(v=VS.85).aspx">XMUINT2</a>
 

 

