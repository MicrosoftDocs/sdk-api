---
UID: NF:directxmath.XMLoadFloat
title: XMLoadFloat function
author: windows-sdk-content
description: Loads a floating-point scalar value into an XMVECTOR.
old-location: dxmath\xmloadfloat.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadFloat(const float)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMLoadFloat, XMLoadFloat, XMLoadFloat method [DirectX Math Support APIs], dxmath.xmloadfloat
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
 - XMLoadFloat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadFloat function


## -description


Loads a floating-point scalar value into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the scalar data to load. The data pointed to by this parameter must be 4-byte aligned and reside in cached
        memory.


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> whose <b>x</b> member is loaded with the data from the
       <i>pSource</i> parameter. The other components of the returned vector will be initialized to 0.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

