---
UID: NF:directxmath.XMLoadInt3
title: XMLoadInt3 function
author: windows-sdk-content
description: Loads data into the x, y, and z components of an XMVECTOR, without type checking.
old-location: dxmath\xmloadint3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt3(const VOID)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMLoadInt3, XMLoadInt3, XMLoadInt3 method [DirectX Math Support APIs], dxmath.xmloadint3
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
 - XMLoadInt3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMLoadInt3
: 
---

# XMLoadInt3 function


## -description


Loads data into the x, y, and z components of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>, without type checking.
<div class="alert"><b>Note</b>  This function is provided for backward compatibility with the Xbox Math library. You should use
  <b>XMLoadInt3</b> when you load integer data, and use
  <a href="https://msdn.microsoft.com/4564cbae-f99b-46dc-91ba-93b8018d17bb">XMLoadFloat3</a> when you load floating point data.</div><div> </div>

## -parameters




### -param pSource [in]

Address of the data to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The w component of the returned <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> is initialized to 0.

To convert the loaded <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> into float values, use
   <a href="https://msdn.microsoft.com/7f93353d-a00b-47a5-b7cb-99b1e79a51f1">XMConvertVectorUIntToFloat</a> or
   <a href="https://msdn.microsoft.com/00db7e6f-af9d-4e8c-a9c0-4451d08f9e10">XMConvertVectorIntToFloat</a>.

The following pseudocode shows you the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR vectorOut;

uint32_t* pElement = (uint32_t*)pSource;

V.u[0] = pElement[0];
V.u[1] = pElement[1];
V.u[2] = pElement[2];
V.u[3] = 0;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>



<a href="https://msdn.microsoft.com/9924ed70-e6f8-4040-aab1-977bc3f197e6">XMINT3</a>



<a href="https://msdn.microsoft.com/b8989871-b4a5-4268-b0ce-0ab6686a3bea">XMLoadSInt3</a>



<a href="https://msdn.microsoft.com/00a7e599-4a1b-4911-942d-7fa6b8d42246">XMLoadUInt3</a>



<a href="https://msdn.microsoft.com/B3B7CD31-8759-4674-AAA9-E13DA1D67675">XMUINT3</a>
 

 

