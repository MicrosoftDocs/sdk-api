---
UID: NF:directxmath.XMVector3TransformStream
title: XMVector3TransformStream function
author: windows-sdk-content
description: Transforms a stream of 3D vectors by a given matrix.
old-location: dxmath\xmvector3transformstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3TransformStream(XMFLOAT4@,size_t,const XMFLOAT3,size_t,size_t,XMMATRIX)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVector3TransformStream, XMVector3TransformStream, XMVector3TransformStream method [DirectX Math Support APIs], dxmath.xmvector3transformstream
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
 - XMVector3TransformStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector3TransformStream
: 
---

# XMVector3TransformStream function


## -description


Transforms a stream of 3D vectors by a given matrix.


## -parameters




### -param pOutputStream [out]

Address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.


### -param OutputStride [in]

Stride, in bytes, between vectors in the destination stream.


### -param pInputStream [in]

Address of the first <a href="https://msdn.microsoft.com/115a901e-ca61-4895-b93f-09b53dbc313f">XMFLOAT3</a> in the stream to be transformed.


### -param InputStride [in]

Stride, in bytes, between vectors in the input stream.


### -param VectorCount [in]

Number of vectors to transform.


### -param M [in]

Transformation matrix.


## -returns



Returns the address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.




## -remarks



<code>XMVector3TransformStream</code> ignores the w component of the input vector, and uses a value of 1.0 instead. The w component of the returned vectors may be non-homogeneous (!= 1.0).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/148972da-e460-63b9-6b01-10201f63d157">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/9331e7fc-d140-43cd-b810-41c03d3041b4">XMVector3Transform</a>
 

 

