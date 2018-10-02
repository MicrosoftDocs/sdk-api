---
UID: NF:directxpackedvector.XMLoadHalf2
title: XMLoadHalf2 function
author: windows-sdk-content
description: Loads an XMHALF2 into an XMVECTOR.
old-location: dxmath\xmloadhalf2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.loading.XMLoadHalf2(const XMHALF2)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DirectX::PackedVector.XMLoadHalf2, XMLoadHalf2, XMLoadHalf2 method [DirectX Math Support APIs], dxmath.xmloadhalf2
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
 - XMLoadHalf2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMLoadHalf2 function


## -description


Loads an <a href="https://msdn.microsoft.com/en-us/library/Ee419652(v=VS.85).aspx">XMHALF2</a> into an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>.


## -parameters




### -param pSource [in]

Address of the <a href="https://msdn.microsoft.com/en-us/library/Ee419652(v=VS.85).aspx">XMHALF2</a> structure to load. 


## -returns



Returns an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a> loaded with the data from the <i>pSource</i> parameter.




## -remarks



The <b>x</b> and <b>y</b> members of the <a href="https://msdn.microsoft.com/en-us/library/Ee419652(v=VS.85).aspx">XMHALF2</a> are converted to
   single-precision format and loaded into the corresponding members of the <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR</a>. The
   <b>z</b> and <b>w</b> members of the returned <b>XMVECTOR</b> will be initialized to 0.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/3434ea7d-edc3-a8eb-3481-9e76ba724800">DirectXMath Library Vector Load Functions</a>
 

 

