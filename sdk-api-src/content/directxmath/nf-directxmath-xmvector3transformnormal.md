---
UID: NF:directxmath.XMVector3TransformNormal
title: XMVector3TransformNormal function
author: windows-sdk-content
description: Transforms the 3D vector normal by the given matrix.
old-location: dxmath\xmvector3transformnormal.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.transformation.XMVector3TransformNormal(XMVECTOR,XMMATRIX)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMVector3TransformNormal, XMVector3TransformNormal, XMVector3TransformNormal method [DirectX Math Support APIs], dxmath.xmvector3transformnormal
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
 - XMVector3TransformNormal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector3TransformNormal
: 
---

# XMVector3TransformNormal function


## -description


Transforms the 3D vector normal by the given matrix.


## -parameters




### -param V [in]

3D normal vector.


### -param M [in]

Transformation matrix.


## -returns



Returns the transformed vector.




## -remarks



<code>XMVector3TransformNormal</code> performs transformations using the input matrix rows 0, 1, and 2 for rotation and scaling, and ignores row 3.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/148972da-e460-63b9-6b01-10201f63d157">DirectXMath Library 3D Vector Transformation Functions</a>



<a href="https://msdn.microsoft.com/c3f0831f-90ad-45e8-9bcc-15967986f671">XMVector3TransformNormalStream</a>
 

 

