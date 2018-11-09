---
UID: NF:directxpackedvector.XMStoreByte4
title: XMStoreByte4 function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMBYTE4.
old-location: dxmath\xmstorebyte4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreByte4(XMBYTE4@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DirectX::PackedVector.XMStoreByte4, XMStoreByte4, XMStoreByte4 method [DirectX Math Support APIs], dxmath.xmstorebyte4
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
 - XMStoreByte4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreByte4 function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/en-us/library/Ee419276(v=VS.85).aspx">XMBYTE4</a>.


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
static const XMVECTOR  Min = {-127.0f, -127.0f, -127.0f, -127.0f};
static const XMVECTOR  Max = {127.0f, 127.0f, 127.0f, 127.0f};

N = XMVectorClamp(V, Min, Max);
N = XMVectorRound(N);

pDestination-&gt;x = (int8_t)N.v[0];
pDestination-&gt;y = (int8_t)N.v[1];
pDestination-&gt;z = (int8_t)N.v[2];
pDestination-&gt;w = (int8_t)N.v[3];
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

