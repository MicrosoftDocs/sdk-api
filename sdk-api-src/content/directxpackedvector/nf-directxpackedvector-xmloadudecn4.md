---
UID: NF:directxpackedvector.XMLoadUDecN4
title: XMLoadUDecN4 function
author: windows-sdk-content
description: Loads an XMUDECN4 into an XMVECTOR.
old-location: dxmath\xmloadudecn4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadUDecN4(const XMUDECN4)
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: DirectX::PackedVector.XMLoadUDecN4, XMLoadUDecN4, XMLoadUDecN4 method [DirectX Math Support APIs], dxmath.xmloadudecn4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXMath.h
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
 - directxpackedvector.h
api_name:
 - XMLoadUDecN4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMLoadUDecN4 function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee420527(v=VS.85).aspx">XMUDECN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee420527(v=VS.85).aspx">XMUDECN4</a> structure to load. 


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

uint32_t Element;

Element = pSource-&gt;v &amp; 0x3FF;
vectorOut.x = (float)Element / 1023.f;
Element = (pSource-&gt;v &gt;&gt; 10) &amp; 0x3FF;
vectorOut.y = (float)Element / 1023.f;
Element = (pSource-&gt;v &gt;&gt; 20) &amp; 0x3FF;
vectorOut.z = (float)Element / 1023.f;
vectorOut.w = (float)(pSource-&gt;v &gt;&gt; 30) / 3.f;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

