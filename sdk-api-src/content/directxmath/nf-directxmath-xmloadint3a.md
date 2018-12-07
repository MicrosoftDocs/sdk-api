---
UID: NF:directxmath.XMLoadInt3A
title: XMLoadInt3A function
author: windows-sdk-content
description: Loads 16-byte aligned data into the x, y, and z components of an XMVECTOR, without type checking.
old-location: dxmath\xmloadint3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt3A(const VOID)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMLoadInt3A, XMLoadInt3A, XMLoadInt3A method [DirectX Math Support APIs], dxmath.xmloadint3a
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
 - XMLoadInt3A
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadInt3A function


## -description


Loads 16-byte aligned data into the <b>x</b>, <b>y</b>, and <b>z</b> components of an
  <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>, without type checking.
<div class="alert"><b>Note</b>  This function is provided for backward compatibility with the Xbox Math library. You should use
  <b>XMLoadInt3A</b> when you load integer data, and
  <a href="https://msdn.microsoft.com/009681d9-8e9b-4436-bd76-0c38c9035d10">XMLoadFloat3A</a> when you load floating point data.</div><div> </div>

## -parameters




### -param pSource [in]

Address of the 16-byte aligned data to load.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The w component of the returned <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> is initialized to 0.

To convert the loaded <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> into float values, use
   <a href="https://msdn.microsoft.com/7f93353d-a00b-47a5-b7cb-99b1e79a51f1">XMConvertVectorUIntToFloat</a> or
   <a href="https://msdn.microsoft.com/00db7e6f-af9d-4e8c-a9c0-4451d08f9e10">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.


```
XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

assert(((uint32_t_PTR)pSource & 0xF) == 0);

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = pElement[2];
V.u[3] = 0;
	
return vectorOut;
```


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

