---
UID: NF:directxmath.XMPlaneIsNaN
title: XMPlaneIsNaN function (directxmath.h)
description: Tests whether any of the coefficients of a plane is a NaN.helpviewer_keywords: ["Use DirectX..XMPlaneIsNaN","XMPlaneIsNaN","XMPlaneIsNaN method [DirectX Math Support APIs]","dxmath.xmplaneisnan"]
old-location: dxmath\xmplaneisnan.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.plane.XMPlaneIsNaN(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMPlaneIsNaN, XMPlaneIsNaN, XMPlaneIsNaN method [DirectX Math Support APIs], dxmath.xmplaneisnan
f1_keywords:
- directxmath/XMPlaneIsNaN
dev_langs:
- c++
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
- XMPlaneIsNaN
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMPlaneIsNaN function


## -description


Tests whether any of the coefficients of a plane is a NaN.


## -parameters




### -param P [in]

<b>XMVECTOR</b> describing the plane coefficients (A, B, C, D) for the plane equation <code>Ax+By+Cz+D=0</code>.


## -returns



Returns true if any of the coefficients of the plane is a NaN, and false otherwise.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-plane">DirectXMath Library Plane Functions</a>
 

 

