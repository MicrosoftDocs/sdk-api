---
UID: NF:directxmath.XMVector2TransformStream
title: XMVector2TransformStream function
author: windows-sdk-content
description: Transforms a stream of 2D vectors by a given matrix.
old-location: dxmath\xmvector2transformstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2TransformStream(XMFLOAT4@,size_t,const XMFLOAT2,size_t,size_t,XMMATRIX)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVector2TransformStream, XMVector2TransformStream, XMVector2TransformStream method [DirectX Math Support APIs], dxmath.xmvector2transformstream
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - XMVector2TransformStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector2TransformStream function


## -description


Transforms a stream of 2D vectors by a given matrix.


## -parameters




### -param pOutputStream [out]

Address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.


### -param OutputStride [in]

Stride, in bytes, between vectors in the destination stream.


### -param pInputStream [in]

Address of the first <a href="https://msdn.microsoft.com/7F53D7CC-CE2C-4F1F-AA24-C11DD537F8EB">XMFLOAT2</a> in the stream to be transformed.


### -param InputStride [in]

Stride, in bytes, between vectors in the input stream.


### -param VectorCount [in]

Number of vectors to transform.


### -param M [in]

Transformation matrix.


## -returns



Returns the address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.




## -remarks



<code>XMVector2TransformStream</code> performs transformations by using the input matrix rows 0 and 1 for rotation and scaling, and row 3 for 
    translation (effectively assuming row 2 is 0).  The w component of the input vector is assumed to be 0.
    The z component of the output vector should be ignored and its w component may be non-homogeneous (!= 1.0).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/175c2073-40ac-06b5-2f0e-495bd74b1502">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/280de489-e7f9-4b84-b13e-5c5e613cc4aa">XMVector2Transform</a>
 

 

