---
UID: NF:directxmath.XMVector3AngleBetweenVectors
title: XMVector3AngleBetweenVectors function (directxmath.h)
author: windows-sdk-content
description: Computes the radian angle between two 3D vectors.
old-location: dxmath\xmvector3anglebetweenvectors.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3AngleBetweenVectors(XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3AngleBetweenVectors, XMVector3AngleBetweenVectors, XMVector3AngleBetweenVectors method [DirectX Math Support APIs], dxmath.xmvector3anglebetweenvectors
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
 - XMVector3AngleBetweenVectors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVector3AngleBetweenVectors function


## -description


Computes the radian angle between two 3D vectors.


## -parameters




### -param V1 [in]

3D vector.


### -param V2 [in]

3D vector.


## -returns



Returns a vector. The radian angle between <i>V1</i> and <i>V2</i> is replicated to each of the components.




## -remarks



If V1 and V2 are normalized 3D vectors, it is faster to use <a href="https://msdn.microsoft.com/en-us/library/Ee420800(v=VS.85).aspx">XMVector3AngleBetweenNormals</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>
 

 

