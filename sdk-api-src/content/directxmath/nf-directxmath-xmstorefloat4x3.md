---
UID: NF:directxmath.XMStoreFloat4x3
title: XMStoreFloat4x3 function
author: windows-sdk-content
description: Stores an XMMATRIX in an XMFLOAT4X3.
old-location: dxmath\xmstorefloat4x3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.storing.XMStoreFloat4x3(XMFLOAT4X3@,XMMATRIX)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMStoreFloat4x3, XMStoreFloat4x3, XMStoreFloat4x3 method [DirectX Math Support APIs], dxmath.xmstorefloat4x3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
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
 - DirectXMath.h
api_name:
 - XMStoreFloat4x3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMStoreFloat4x3 function


## -description


Stores an <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a> in an <a href="https://msdn.microsoft.com/56bf0a03-e3ea-43ed-a57e-b53f41348ffa">XMFLOAT4X3</a>.


## -parameters




### -param pDestination [out]

Address at which to store the data.


### -param M [in]

Matrix containing the data to store.


## -returns



None.




## -remarks




<a href="https://msdn.microsoft.com/56bf0a03-e3ea-43ed-a57e-b53f41348ffa">XMFLOAT4X3</a> is a row-major matrix form. This function cannot be used to write out column-major data since it assumes the last column is 0 0 0 1.

This function takes a matrix and writes the components out to twelve single-precision floating-point values at the given
    address. The most significant component of the first row vector is written to the first four bytes of the address,
    followed by the second most significant component of the first row, followed by the third most significant component
    of the first row. The most significant three components of the second row are then written out in a like manner to
    memory beginning at byte 12, followed by the third row to memory beginning at byte 24, and finally the fourth row to
    memory beginning at byte 36.

The following pseudocode demonstrates the operation of the function.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>pDestination-&gt;_11 = M[0].x; // 4 bytes to address (uint8_t*)pDestination
pDestination-&gt;_12 = M[0].y; // 4 bytes to address (uint8_t*)pDestination + 4
pDestination-&gt;_13 = M[0].z; // 4 bytes to address (uint8_t*)pDestination + 8

pDestination-&gt;_21 = M[1].x; // 4 bytes to address (uint8_t*)pDestination + 12
pDestination-&gt;_22 = M[1].y; // 4 bytes to address (uint8_t*)pDestination + 16
pDestination-&gt;_23 = M[1].z; // 4 bytes to address (uint8_t*)pDestination + 20

pDestination-&gt;_31 = M[2].x; // 4 bytes to address (uint8_t*)pDestination + 24
pDestination-&gt;_32 = M[2].y; // 4 bytes to address (uint8_t*)pDestination + 28
pDestination-&gt;_33 = M[2].z; // 4 bytes to address (uint8_t*)pDestination + 32

pDestination-&gt;_41 = M[3].x; // 4 bytes to address (uint8_t*)pDestination + 36
pDestination-&gt;_42 = M[3].y; // 4 bytes to address (uint8_t*)pDestination + 40
pDestination-&gt;_43 = M[3].z; // 4 bytes to address (uint8_t*)pDestination + 44</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/0e7b66bd-bdb0-956d-2962-b33ae52b3016">DirectXMath Library Vector Store Functions</a>
 

 

