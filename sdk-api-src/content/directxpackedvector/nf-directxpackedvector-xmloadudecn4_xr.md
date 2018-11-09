---
UID: NF:directxpackedvector.XMLoadUDecN4_XR
title: XMLoadUDecN4_XR function
author: windows-sdk-content
description: Loads an extended range XMUDECN4 into an XMVECTOR.
old-location: dxmath\_xmloadudecn4_xr.htm
tech.root: dxmath
ms.assetid: C67EEA1C-C416-4E8F-A0D9-F061EF1CD119
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DirectX::PackedVector.XMLoadUDecN4_XR, XMLoadUDecN4_XR, XMLoadUDecN4_XR method [DirectX Math Support APIs], dxmath._xmloadudecn4_xr
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxpackedvector.inl
api_name:
 - XMLoadUDecN4_XR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadUDecN4_XR function


## -description


Loads an extended range <a href="https://msdn.microsoft.com/en-us/library/Ee420527(v=VS.85).aspx">XMUDECN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>. This type loads a 10:10:10:2 normalized GPU format using the Extended Range (XR) with the color bias set to match DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM.


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

int32_t Element;

Element = pSource-&gt;v &amp; 0x3FF;
vectorOut.x = (float)(Element - 0x180) / 510.f;
Element = (pSource-&gt;v &gt;&gt; 10) &amp; 0x3FF;
vectorOut.y = (float)(Element - 0x180) / 510.f;
Element = (pSource-&gt;v &gt;&gt; 20) &amp; 0x3FF;
vectorOut.z = (float)(Element - 0x180) / 510.f;
vectorOut.w = (float)(pSource-&gt;v &gt;&gt; 30) / 3.f;

return vectorOut;</pre>
</td>
</tr>
</table></span></div>
For more details on the Extended Range (XR) with Bias conversion, see <a href="https://msdn.microsoft.com/B3014241-A86A-4B6E-BC9D-50057B924D98">XR_BIAS Color Channel Conversion Rules</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>



<a href="https://msdn.microsoft.com/4DCE74D6-48CF-43D8-BF69-368A95F823F1">XMStoreUDecN4_XR</a>
 

 

