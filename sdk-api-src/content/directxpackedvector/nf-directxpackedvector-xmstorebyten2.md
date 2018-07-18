---
UID: NF:directxpackedvector.XMStoreByteN2
title: XMStoreByteN2 function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMBYTEN2.
old-location: dxmath\xmstorebyten2.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreByteN2(XMBYTEN2@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: DirectX::PackedVector.XMStoreByteN2, XMStoreByteN2, XMStoreByteN2 method [DirectX Math Support APIs], dxmath.xmstorebyten2
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
 - XMStoreByteN2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMStoreByteN2 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/library/Hh437850(v=VS.85).aspx">XMBYTEN2</a>.


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
<pre>
XMVECTOR N;	
static const XMVECTOR  Scale = {127.0f, 127.0f, 127.0f, 127.0f};

N = XMVectorMultiply(V, Scale);
N = XMVectorRound(N);

pDestination-&gt;x = (int8_t)N.v[0];
pDestination-&gt;y = (int8_t)N.v[1];
    
    </pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

