---
UID: NF:directxmath.XMLoadInt2
title: XMLoadInt2 function
author: windows-sdk-content
description: Loads data into the x and y components of an XMVECTOR.
old-location: dxmath\xmloadint2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadInt2(const uint32_t)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMLoadInt2, XMLoadInt2, XMLoadInt2 method [DirectX Math Support APIs], dxmath.xmloadint2
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
 - XMLoadInt2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMLoadInt2
: 
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

To convert the loaded <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> into float values, use <a href="https://msdn.microsoft.com/7f93353d-a00b-47a5-b7cb-99b1e79a51f1">XMConvertVectorUIntToFloat</a> or <a href="https://msdn.microsoft.com/00db7e6f-af9d-4e8c-a9c0-4451d08f9e10">XMConvertVectorIntToFloat</a>.

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
V.u[2] = 0;
V.u[3] = 0;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>



<a href="https://msdn.microsoft.com/41e10329-9f6f-446f-9640-6c1d65e20cb5">XMINT2</a>



<a href="https://msdn.microsoft.com/5bd5a4ee-1438-4cbd-8394-3ee7f002fbf6">XMLoadSInt2</a>



<a href="https://msdn.microsoft.com/2dc3964f-9c5f-44c6-ae3f-6cc79e8f5470">XMLoadUInt2</a>



<a href="https://msdn.microsoft.com/33240440-20A8-4320-AF2F-40BA287CB107">XMUINT2</a>
 

 

