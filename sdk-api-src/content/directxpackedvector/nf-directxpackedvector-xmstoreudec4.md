---
UID: NF:directxpackedvector.XMStoreUDec4
title: XMStoreUDec4 function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMUDEC4.
old-location: dxmath\xmstoreudec4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreUDec4(XMUDEC4@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: DirectX::PackedVector.XMStoreUDec4, XMStoreUDec4, XMStoreUDec4 method [DirectX Math Support APIs], dxmath.xmstoreudec4
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
 - XMStoreUDec4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMStoreUDec4 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/library/Ee420508(v=VS.85).aspx">XMUDEC4</a>.


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
static const XMVECTOR  Max = {1023.0f, 1023.0f, 1023.0f, 3.0f};

assert(pDestination);

N = XMVectorClamp(V, XMVectorZero(), Max);

pDestination-&gt;v = ((uint32_t)N.v[3] &lt;&lt; 30) |
                  (((uint32_t)N.v[2] &amp; 0x3FF) &lt;&lt; 20) |
                  (((uint32_t)N.v[1] &amp; 0x3FF) &lt;&lt; 10) |
                  (((uint32_t)N.v[0] &amp; 0x3FF));</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

