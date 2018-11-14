---
UID: NF:directxmath.XMLoadSInt4
title: XMLoadSInt4 function
author: windows-sdk-content
description: Loads signed integer data into an XMVECTOR.
old-location: dxmath\xmloadsint4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadSInt4(const XMINT4)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMLoadSInt4, XMLoadSInt4, XMLoadSInt4 method [DirectX Math Support APIs], dxmath.xmloadsint4
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
 - XMLoadSInt4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMLoadSInt4
: 
---

# XMLoadSInt4 function


## -description


Loads signed integer data into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of an <a href="https://msdn.microsoft.com/4562AF48-FC7E-4737-AB7B-7A76789DC70B">XMINT4</a> structure containing the data to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i>parameter.




## -remarks



For 16-byte aligned memory, it may be faster to use <a href="https://msdn.microsoft.com/eb545b5a-9132-4c8f-838b-dc528489a6ed">XMLoadInt4A</a> with a casting operator.

The following pseudocode shows the operation of this function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
XMVECTOR vectorOut;

vectorOut.x = (float)pSource-&gt;x;
vectorOut.y = (float)pSource-&gt;y;
vectorOut.z = (float)pSource-&gt;z;
vectorOut.w = (float)pSource-&gt;w;

return vectorOut;
   
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

