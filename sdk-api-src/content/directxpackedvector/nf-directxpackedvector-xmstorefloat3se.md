---
UID: NF:directxpackedvector.XMStoreFloat3SE
title: XMStoreFloat3SE function
author: windows-sdk-content
description: Stores an XMVECTOR in an XMFLOAT3SE.
old-location: dxmath\xmstorefloat3se.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat3SE(XMFLOAT3SE@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DirectX::PackedVector.XMStoreFloat3SE, XMStoreFloat3SE, XMStoreFloat3SE method [DirectX Math Support APIs], dxmath.xmstorefloat3se
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
 - XMStoreFloat3SE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreFloat3SE function


## -description


Stores an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> in an <a href="https://msdn.microsoft.com/A0FE96C6-42AB-411D-874E-E02E0E81CAF0">XMFLOAT3SE</a>.


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

  static const XMVECTOR  Max = { 65472.f, 65427.f, 65427.f, 0 };
  N = XMVectorClamp(V, XMVectorZero(), Max);

  uint32_t m[3], e[3];
  ConvertToFloat14( N.x, &amp;m[0], &amp;e[0]);
  ConvertToFloat14( N.y, &amp;m[1], &amp;e[1]);
  ConvertToFloat14( N.z, &amp;m[2], &amp;e[2]);

  uint32_t T = XMMax( e[0], XMMax( e[1], e[2] ) );

  pDestination-&gt;xm = m[0] &gt;&gt; (T - e[0]);
  PDestination-&gt;ym = m[1] &gt;&gt; (T - e[1]);
  pDestination-&gt;zm = m[2] &gt;&gt; (T - e[2]);
  pDestination-&gt;e = T;
</pre>
</td>
</tr>
</table></span></div>
If the three components are not close to each other in magnitude, the largest value(s) will set the exponent and the
   other components will be shifted to zero.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

