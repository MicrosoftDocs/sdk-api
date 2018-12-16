---
UID: NF:directxmath.XMVectorGetIntZPtr
title: XMVectorGetIntZPtr function
author: windows-sdk-content
description: Retrieves the z component of an XMVECTOR Data Type containing integer data, and stores that component's value in an instance of uint32_t referred to by a pointer.
old-location: dxmath\xmvectorgetintzptr.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.accessors.XMVectorGetIntZPtr(uint32_t@,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Use DirectX..XMVectorGetIntZPtr, XMVectorGetIntZPtr, XMVectorGetIntZPtr method [DirectX Math Support APIs], dxmath.xmvectorgetintzptr
ms.topic: function
req.header: directxmath.h
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
 - directxmathvector.inl
api_name:
 - XMVectorGetIntZPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVectorGetIntZPtr function


## -description


Retrieves the <code>z</code> component of an <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> containing integer data, and stores that
  component's value in an instance of uint32_t referred to by a pointer.


## -parameters




### -param z [out]

Pointer to a uint32_t that will receive the value of the <code>z</code> element of the <a href="https://msdn.microsoft.com/1a044094-444d-e787-fa6a-76e88531aef1">XMVECTOR Data Type</a> object
        <code>V</code>.


### -param V

A valid 4D vector storing integer data.


## -returns



None.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/6e7453b8-0dee-6fc5-cbac-fe20e4e3ef60">DirectXMath Library Vector Accessor Functions</a>
 

 

