---
UID: NF:directxmath.XMLoadFloat3x3
title: XMLoadFloat3x3 function
author: windows-sdk-content
description: Loads an XMFLOAT3X3 into an XMMATRIX.
old-location: dxmath\xmloadfloat3x3.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3x3(const XMFLOAT3X3)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMLoadFloat3x3, XMLoadFloat3x3, XMLoadFloat3x3 method [DirectX Math Support APIs], dxmath.xmloadfloat3x3
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
 - XMLoadFloat3x3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadFloat3x3 function


## -description


Loads an <a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a> into an <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a> structure to load. This parameter must point to cached
        memory.


## -returns



Returns an <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a> loaded with the data from the <i>pSource</i> parameter.

This function performs a partial load of the returned <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>. See <a href="https://msdn.microsoft.com/9972e382-7a0f-88a7-ad44-18521af3520d">Getting Started</a> for more information.




## -remarks




<a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a> is a row-major form of the matrix. This function could be used to read column-major data, 
    but would then need to be transposed with <a href="https://msdn.microsoft.com/6267c6c3-1fda-44b1-8809-f0ad8988a49f">XMMatrixTranpose</a> before use in other XMMATRIX functions.

The members of the <a href="https://msdn.microsoft.com/6067d4b2-8609-4172-8228-5e3d43638015">XMFLOAT3X3</a> structures (<b>_11</b>, <b>_12</b>,
   <b>_13</b>, and so on) are loaded into the corresponding members of the
   <a href="https://msdn.microsoft.com/64dd4128-103b-4d54-98f3-cc908170d81c">XMMATRIX</a>. The remaining members of the returned
   <b>XMMATRIX</b> are 0.0f, except for <b>_44</b>, which is 1.0f.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

