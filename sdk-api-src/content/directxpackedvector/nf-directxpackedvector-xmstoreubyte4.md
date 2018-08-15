---
UID: NF:directxpackedvector.XMStoreUByte4
title: XMStoreUByte4 function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMUBYTE4.
old-location: dxmath\xmstoreubyte4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreUByte4(XMUBYTE4@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMStoreUByte4, XMStoreUByte4, XMStoreUByte4 method [DirectX Math Support APIs], dxmath.xmstoreubyte4
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
 - XMStoreUByte4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMStoreUByte4 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/210300b6-9bf2-4ac4-94e3-b2df2d228365">XMUBYTE4</a>.


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
static const XMVECTOR  Max = {255.0f, 255.0f, 255.0f, 255.0f};

assert(pDestination);

N = XMVectorClamp(V, XMVectorZero(), Max);
N = XMVectorRound(N);

pDestination-&gt;x = (uint8_t)N.v[0];
pDestination-&gt;y = (uint8_t)N.v[1];
pDestination-&gt;z = (uint8_t)N.v[2];
pDestination-&gt;w = (uint8_t)N.v[3];</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

