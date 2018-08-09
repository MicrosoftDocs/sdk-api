---
UID: NF:directxpackedvector.XMLoadHalf4
title: XMLoadHalf4 function
author: windows-sdk-content
description: Loads an XMHALF4 into an XMVECTOR.
old-location: dxmath\xmloadhalf4.htm
old-project: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadHalf4(const XMHALF4)
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DirectX::PackedVector.XMLoadHalf4, XMLoadHalf4, XMLoadHalf4 method [DirectX Math Support APIs], dxmath.xmloadhalf4
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: directxpackedvector.h
req.include-header: DirectXMath.h
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
 - directxpackedvector.h
api_name:
 - XMLoadHalf4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# XMLoadHalf4 function


## -description


Loads an <a href="https://msdn.microsoft.com/194CC053-8341-4E26-B8B2-5F137B201D80">XMHALF4</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/194CC053-8341-4E26-B8B2-5F137B201D80">XMHALF4</a> structure to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The four half-precision floating-point members of the <a href="https://msdn.microsoft.com/194CC053-8341-4E26-B8B2-5F137B201D80">XMHALF4</a> are converted to
   single-precision format and loaded into the corresponding members of the <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

