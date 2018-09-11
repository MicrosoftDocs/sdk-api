---
UID: NF:directxmath.XMLoadFloat3A
title: XMLoadFloat3A function
author: windows-sdk-content
description: Loads an XMFLOAT3A into an XMVECTOR.
old-location: dxmath\xmloadfloat3a.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat3A(const XMFLOAT3A)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Use DirectX..XMLoadFloat3A, XMLoadFloat3A, XMLoadFloat3A method [DirectX Math Support APIs], dxmath.xmloadfloat3a
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
 - XMLoadFloat3A
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadFloat3A function


## -description


Loads an <a href="https://msdn.microsoft.com/bad51162-3eaa-44e1-9032-6db3e75f0e99">XMFLOAT3A</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/bad51162-3eaa-44e1-9032-6db3e75f0e99">XMFLOAT3A</a> structure to load.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The <b>x</b>, <b>y</b>, and <b>z</b> members of the <a href="https://msdn.microsoft.com/bad51162-3eaa-44e1-9032-6db3e75f0e99">XMFLOAT3A</a> are loaded
   into the corresponding members of the returned <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>. The <b>w</b> member of the
   <b>XMVECTOR</b> is initialized to 0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

