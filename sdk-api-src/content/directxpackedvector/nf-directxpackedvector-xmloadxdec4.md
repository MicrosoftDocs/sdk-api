---
UID: NF:directxpackedvector.XMLoadXDec4
title: XMLoadXDec4 function
author: windows-sdk-content
description: Loads an XMXDEC4 into an XMVECTOR.
old-location: dxmath\xmloadxdec4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadXDec4(const XMXDEC4)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMLoadXDec4, XMLoadXDec4, XMLoadXDec4 method [DirectX Math Support APIs], dxmath.xmloadxdec4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXMath.h
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
 - directxpackedvector.h
api_name:
 - XMLoadXDec4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMLoadXDec4 function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee421399(v=VS.85).aspx">XMXDEC4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee421399(v=VS.85).aspx">XMXDEC4</a> structure to load. 


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
static const uint32_t SignExtend[] = {0x00000000, 0xFFFFFC00};

Element = pSource-&gt;v &amp; 0x3FF;
vectorOut.x = (float)(int16_t)(Element | SignExtend[Element &gt;&gt; 9]);
Element = (pSource-&gt;v &gt;&gt; 10) &amp; 0x3FF;
vectorOut.y = (float)(int16_t)(Element | SignExtend[Element &gt;&gt; 9]);
Element = (pSource-&gt;v &gt;&gt; 20) &amp; 0x3FF;
vectorOut.z = (float)(int16_t)(Element | SignExtend[Element &gt;&gt; 9]);
vectorOut.w = (float)(pSource-&gt;v &gt;&gt; 30);

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

