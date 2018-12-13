---
UID: NF:directxmath.XMLoadInt4A
title: XMLoadInt4A function
author: windows-sdk-content
description: Loads 16-byte aligned data into an XMVECTOR, without type checking.
old-location: dxmath\xmloadint4a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt4A(const VOID)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMLoadInt4A, XMLoadInt4A, XMLoadInt4A method [DirectX Math Support APIs], dxmath.xmloadint4a
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMLoadInt4A
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadInt4A function


## -description


Loads 16-byte aligned data into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>, without type checking.
<div class="alert"><b>Note</b>  This function is provided for backward compatibility with the Xbox Math library. It is recommended that
  <b>XMLoadInt4A</b> be used when loading integer data and
  <a href="https://msdn.microsoft.com/865dcc01-8b54-4d4e-831c-0bed7b358292">XMLoadFloat4A</a> be used when loading floating point data.</div><div> </div>

## -parameters




### -param pSource [in]

Address of the 16-byte aligned data to load.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



To convert the loaded <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> into float values, use <a href="https://msdn.microsoft.com/en-us/library/Hh437937(v=VS.85).aspx">XMConvertVectorUIntToFloat</a> or <a href="https://msdn.microsoft.com/en-us/library/Hh437934(v=VS.85).aspx">XMConvertVectorIntToFloat</a>.

The following pseudocode demonstrates the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

assert(((uint32_t_PTR)pSource & 0xF) == 0);

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = pElement[2];
V.u[3] = pElement[3];
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

