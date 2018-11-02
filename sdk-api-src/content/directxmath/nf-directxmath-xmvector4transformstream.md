---
UID: NF:directxmath.XMVector4TransformStream
title: XMVector4TransformStream function
author: windows-sdk-content
description: Transforms a stream of 4D vectors by a given matrix.
old-location: dxmath\xmvector4transformstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector4TransformStream(XMFLOAT4@,size_t,const XMFLOAT4,size_t,size_t,XMMATRIX)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector4TransformStream, XMVector4TransformStream, XMVector4TransformStream method [DirectX Math Support APIs], dxmath.xmvector4transformstream
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
 - XMVector4TransformStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector4TransformStream
: 
---

# XMVector4TransformStream function


## -description


Transforms a stream of 4D vectors by a given matrix.


## -parameters




### -param pOutputStream [out]

Address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.


### -param OutputStride [in]

Stride, in bytes, between vectors in the destination stream.


### -param pInputStream [in]

Address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the stream to be transformed.


### -param InputStride [in]

Stride, in bytes, between vectors in the input stream.


### -param VectorCount [in]

Number of vectors to transform.


### -param M [in]

Transformation matrix.


## -returns



Returns the address of the first <a href="https://msdn.microsoft.com/2af4929b-9e44-4229-916e-d7d8eae07306">XMFLOAT4</a> in the destination stream.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/25fada4c-0ddc-0b79-9b8a-e9edfefce19a">DirectXMath Library 4D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/58CB8AD1-3FF2-43A2-8FE2-F20C04080B57">XMVector4Transform</a>
 

 

