---
UID: NF:directxmath.XMLoadFloat4x4
title: XMLoadFloat4x4 function
author: windows-sdk-content
description: Loads an XMFLOAT4X4 into an XMMATRIX.
old-location: dxmath\xmloadfloat4x4.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat4x4(const XMFLOAT4X4)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMLoadFloat4x4, XMLoadFloat4x4, XMLoadFloat4x4 method [DirectX Math Support APIs], dxmath.xmloadfloat4x4
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
 - XMLoadFloat4x4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadFloat4x4 function


## -description


Loads an <a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a> into an <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a> structure to load.


## -returns



Returns an <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks




<a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a> is a row-major form of the matrix. This function could be used to read column-major data, 
    but would then need to be transposed with <a href="https://msdn.microsoft.com/6267c6c3-1fda-44b1-8809-f0ad8988a49f">XMMatrixTranpose</a> before use in other XMMATRIX functions.

The members of the <a href="https://msdn.microsoft.com/92991b18-60a5-41ec-85de-690ac6e5f1e2">XMFLOAT4X4</a> structure (<b>_11</b>, <b>_12</b>,
    <b>_13</b>, and so on) are loaded into the corresponding members of the
    <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

