---
UID: NF:directxmath.XMQuaternionLn
title: XMQuaternionLn function (directxmath.h)
description: Computes the natural logarithm of a given unit quaternion.helpviewer_keywords: ["Use DirectX..XMQuaternionLn","XMQuaternionLn","XMQuaternionLn method [DirectX Math Support APIs]","dxmath.xmquaternionln"]
old-location: dxmath\xmquaternionln.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionLn(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionLn, XMQuaternionLn, XMQuaternionLn method [DirectX Math Support APIs], dxmath.xmquaternionln
f1_keywords:
- directxmath/XMQuaternionLn
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
- XMQuaternionLn
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMQuaternionLn function


## -description


Computes the natural logarithm of a given unit quaternion.


## -parameters




### -param Q [in]

Unit quaternion for which to calculate the natural logarithm. If <i>Q</i> is not a unit quaternion, the returned
        value is undefined.


## -returns



Returns the natural logarithm of <i>Q</i>.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
 

 

