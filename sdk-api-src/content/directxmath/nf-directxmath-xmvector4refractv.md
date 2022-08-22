---
UID: NF:directxmath.XMVector4RefractV
title: XMVector4RefractV function (directxmath.h)
description: Refracts an incident 4D vector across a 4D normal vector. (XMVector4RefractV)
helpviewer_keywords: ["Use DirectX..XMVector4RefractV","XMVector4RefractV","XMVector4RefractV method [DirectX Math Support APIs]","dxmath.xmvector4refractv"]
old-location: dxmath\xmvector4refractv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector4RefractV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector4RefractV, XMVector4RefractV, XMVector4RefractV method [DirectX Math Support APIs], dxmath.xmvector4refractv
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMVector4RefractV
 - directxmath/XMVector4RefractV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directxmathvector.inl
api_name:
 - XMVector4RefractV
---

# XMVector4RefractV function


## -description

Refracts an incident 4D vector across a 4D normal vector.

## -parameters

### -param Incident [in]

4D incident vector to refract.

### -param Normal [in]

4D normal vector to refract the incident vector through.

### -param RefractionIndex [in]

4D vector, all of whose components are equal to the index of refraction.

## -returns

Returns the refracted incident vector. If the refraction index and the angle between the incident vector and the normal are such that the result is a total internal reflection, the function will return a vector of the form &lt; 0.0f, 0.0f, 0.0f, 0.0f &gt;.

## -remarks

This function is identical to <a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4refract">XMVector4Refract</a> except that the <i>RefractionIndex</i> is supplied using a 4D vector instead of a <b>float</b> value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector4-geometric">DirectXMath Library 4D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector4refract">XMVector4Refract</a>
