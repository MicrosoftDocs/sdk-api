---
UID: NF:directxpackedvector.XMLoadByteN4
title: XMLoadByteN4 function
author: windows-sdk-content
description: Loads an XMBYTEN4 into an XMVECTOR.
old-location: dxmath\xmloadbyten4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadByteN4(const XMBYTEN4)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMLoadByteN4, XMLoadByteN4, XMLoadByteN4 method [DirectX Math Support APIs], dxmath.xmloadbyten4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXPackedVector.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxpackedvector.inl
api_name:
 - XMLoadByteN4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMLoadByteN4 function


## -description


Loads an <a href="https://msdn.microsoft.com/62d61a35-8674-4855-b09c-f351363cd50b">XMBYTEN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/62d61a35-8674-4855-b09c-f351363cd50b">XMBYTEN4</a> structure to load. 


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

vectorOut.x = (float)pSource-&gt;x / 127.0f;
vectorOut.y = (float)pSource-&gt;y / 127.0f;
vectorOut.z = (float)pSource-&gt;z / 127.0f;
vectorOut.w = (float)pSource-&gt;w / 127.0f;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
Note that both -127 and -128 map to -1.f.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

