---
UID: NF:directxpackedvector.XMStoreUDecN4_XR
title: XMStoreUDecN4_XR function
author: windows-sdk-content
description: Stores an extended range XMUDECN4 into an XMVECTOR.
old-location: dxmath\_xmstoreudecn4_xr.htm
old-project: dxmath
ms.assetid: 4DCE74D6-48CF-43D8-BF69-368A95F823F1
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: DirectX::PackedVector.XMStoreUDecN4_XR, XMStoreUDecN4_XR, XMStoreUDecN4_XR method [DirectX Math Support APIs], dxmath._xmstoreudecn4_xr
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
 - XMStoreUDecN4_XR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMStoreUDecN4_XR function


## -description


Stores an extended range <a href="https://msdn.microsoft.com/library/Ee420527(v=VS.85).aspx">XMUDECN4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>. This type stores a 10:10:10:2 normalized GPU format using the Extended Range (XR) with the color bias set to match DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM.


## -parameters




### -param pDestination [out]

Address at which to store the data.


### -param V [in]

Vector containing the data to store.


## -returns



None.




## -remarks



The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>XMVECTOR N; 
static const XMVECTOR Scale = {510.0f, 510.0f, 510.0f, 3.0f};
static const XMVECTOR Bias = { 384.0f, 384.0f, 384.0f, 0.0f };
static const XMVECTOR C = { 1023.f, 1023.f, 1023.f, 3.f };

assert(pDestination);

N = XMVectorMultiplyAdd( V, Scale, Bias );
N = XMVectorClamp( V, XMVectorZero(), C );

pDestination-&gt;v = ((uint32_t)N.v[3] &lt;&lt; 30) |
(((uint32_t)N.v[2] &amp; 0x3FF) &lt;&lt; 20) |
(((uint32_t)N.v[1] &amp; 0x3FF) &lt;&lt; 10) |
(((uint32_t)N.v[0] &amp; 0x3FF));</pre>
</td>
</tr>
</table></span></div>
For more details on the Extended Range (XR) with Bias conversion, see <a href="https://msdn.microsoft.com/B3014241-A86A-4B6E-BC9D-50057B924D98">XR_BIAS Color Channel Conversion Rules</a>. 

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>



<a href="https://msdn.microsoft.com/C67EEA1C-C416-4E8F-A0D9-F061EF1CD119">XMLoadUDecN4_XR</a>
 

 

