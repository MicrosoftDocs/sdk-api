---
UID: NF:directxmath.XMQuaternionConjugate
title: XMQuaternionConjugate function (directxmath.h)
description: Computes the conjugate of a quaternion.helpviewer_keywords: ["Use DirectX..XMQuaternionConjugate","XMQuaternionConjugate","XMQuaternionConjugate method [DirectX Math Support APIs]","dxmath.xmquaternionconjugate"]
old-location: dxmath\xmquaternionconjugate.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.quaternion.XMQuaternionConjugate(XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMQuaternionConjugate, XMQuaternionConjugate, XMQuaternionConjugate method [DirectX Math Support APIs], dxmath.xmquaternionconjugate
f1_keywords:
- directxmath/XMQuaternionConjugate
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
- XMQuaternionConjugate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMQuaternionConjugate function


## -description


Computes the conjugate of a quaternion.


## -parameters




### -param Q [in]

The quaternion to conjugate.


## -returns



Returns the conjugate of <i>Q</i>.




## -remarks



The DirectXMath quaternion functions use an XMVECTOR 4-vector to represent quaternions, 
    where the X, Y, and Z components are the vector part and the W component is the scalar part.

Given a quaternion (
   <i>x</i>,
   <i>y</i>,
   <i>z</i>,
   <i>w</i>), the <code>XMQuaternionConjugate</code> function returns the quaternion (-
   <i>x</i>, -
   <i>y</i>, -
   <i>z</i>,
   <i>w</i>).

Use the <a href="https://docs.microsoft.com/windows/desktop/api/directxmath/nf-directxmath-xmquaternionnormalize">XMQuaternionNormalize</a> function for any quaternion input
   that is not already normalized.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dxmath/ovw-xnamath-reference-functions-quaternion">DirectXMath Library Quaternion Functions</a>
 

 

