---
UID: NF:directxmath.XMVector3Refract
title: XMVector3Refract function (directxmath.h)
description: Refracts an incident 3D vector across a 3D normal vector. (XMVector3Refract)
helpviewer_keywords: ["Use DirectX..XMVector3Refract","XMVector3Refract","XMVector3Refract method [DirectX Math Support APIs]","dxmath.xmvector3refract"]
old-location: dxmath\xmvector3refract.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3Refract(XMVECTOR,XMVECTOR,float)
ms.date: 12/05/2018
ms.keywords: Use DirectX..XMVector3Refract, XMVector3Refract, XMVector3Refract method [DirectX Math Support APIs], dxmath.xmvector3refract
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
 - XMVector3Refract
 - directxmath/XMVector3Refract
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
 - XMVector3Refract
---

# XMVector3Refract function


## -description

Refracts an incident 3D vector across a 3D normal vector.

## -parameters

### -param Incident [in]

3D incident vector to refract.

### -param Normal [in]

3D normal vector to refract the incident vector through.

### -param RefractionIndex [in]

Index of refraction. See remarks.

## -returns

Returns the refracted incident vector. If the refraction index and the angle between the incident vector and the normal are such that the result is a total internal reflection, the function will return a vector of the form &lt; 0.0f, 0.0f, 0.0f, undefined &gt;.

## -remarks

The following pseudocode demonstrates the operation of the function:


```
XMVECTOR Result;

float t = ( Incident.x * Normal.x + Incident.y * Normal.y + Incident.z * Normal.z );
float r = 1.0f - RefractionIndex * RefractionIndex * (1.0f - t * t);

if (r < 0.0f) // Total internal reflection
{
	Result.x = 0.0f;
	Result.y = 0.0f;
	Result.z = 0.0f;
}
else
{
	float s = RefractionIndex * t + sqrt(r);
	Result.x = RefractionIndex * Incident.x - s * Normal.x;
	Result.y = RefractionIndex * Incident.y - s * Normal.y;
	Result.z = RefractionIndex * Incident.z - s * Normal.z;
}

Result.w = undefined;

return Result;
```


The index of refraction is the ratio of the index of refraction of the medium containing the incident vector to the index of refraction of the medium being entered (where the index of refraction of a medium is itself the ratio of the speed of light in a vacuum to the speed of light in the medium).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

<a href="/windows/desktop/dxmath/ovw-xnamath-reference-functions-vector3-geometric">DirectXMath Library 3D Vector Geometric Functions</a>



<a href="/windows/desktop/api/directxmath/nf-directxmath-xmvector2refractv">XMVector2RefractV</a>
