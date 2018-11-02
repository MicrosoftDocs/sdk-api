---
UID: NF:directxmath.XMVector2TransformNormalStream
title: XMVector2TransformNormalStream function
author: windows-sdk-content
description: Transforms a stream of 2D normal vectors by a given matrix.
old-location: dxmath\xmvector2transformnormalstream.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector2TransformNormalStream(XMFLOAT2@,size_t,const XMFLOAT2,size_t,size_t,XMMATRIX)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector2TransformNormalStream, XMVector2TransformNormalStream, XMVector2TransformNormalStream method [DirectX Math Support APIs], dxmath.xmvector2transformnormalstream
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
 - XMVector2TransformNormalStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector2TransformNormalStream
: 
---

# XMVector2TransformNormalStream function


## -description


Transforms a stream of 2D normal vectors by a given matrix.


## -parameters




### -param pOutputStream [out]

Address of the first <a href="https://msdn.microsoft.com/7F53D7CC-CE2C-4F1F-AA24-C11DD537F8EB">XMFLOAT2</a> in the destination stream.


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



Returns the address of the first <a href="https://msdn.microsoft.com/7F53D7CC-CE2C-4F1F-AA24-C11DD537F8EB">XMFLOAT2</a> in the destination stream.




## -remarks



Each vector in the input stream must be normalized.

<code>XMVector2TransformNormalStream</code> uses row 0 and 1 of the input transformation matrix for rotation and scaling.  Rows 2 and 3 are ignored.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/175c2073-40ac-06b5-2f0e-495bd74b1502">DirectXMath Library 2D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/651149dd-f797-4d34-9750-d68ba87f4cbb">XMVector2TransformNormal</a>
 

 

