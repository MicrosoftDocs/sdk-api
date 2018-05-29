---
UID: NF:directxpackedvector.XMLoadShortN4
title: XMLoadShortN4 function
author: windows-sdk-content
description: Loads an XMSHORTN4 into an XMVECTOR.
old-location: dxmath\xmloadshortn4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadShortN4(const XMSHORTN4)
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: DirectX::PackedVector.XMLoadShortN4, XMLoadShortN4, XMLoadShortN4 method [DirectX Math Support APIs], dxmath.xmloadshortn4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: DirectX::PackedVector
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	directxpackedvector.inl
api_name:
-	XMLoadShortN4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMLoadShortN4 function


## -description


Loads an <a href="https://msdn.microsoft.com/1dfe894e-bc5f-4bfd-a4ba-71fb3e4c9728">XMSHORTN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/1dfe894e-bc5f-4bfd-a4ba-71fb3e4c9728">XMSHORTN4</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR vectorOut;

vectorOut.x = (float)pSource-&gt;x / 32767.0f;
vectorOut.y = (float)pSource-&gt;y / 32767.0f;
vectorOut.z = (float)pSource-&gt;z / 32767.0f;
vectorOut.w = (float)pSource-&gt;w / 32767.0f;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
Note that both -32767 and -32768 map to -1.f.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

