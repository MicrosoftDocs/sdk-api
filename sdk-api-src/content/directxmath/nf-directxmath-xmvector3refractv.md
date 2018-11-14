---
UID: NF:directxmath.XMVector3RefractV
title: XMVector3RefractV function
author: windows-sdk-content
description: Refracts an incident 3D vector across a 3D normal vector.
old-location: dxmath\xmvector3refractv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector3RefractV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Use DirectX..XMVector3RefractV, XMVector3RefractV, XMVector3RefractV method [DirectX Math Support APIs], dxmath.xmvector3refractv
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
 - XMVector3RefractV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector3RefractV
: 
---

# XMVector3RefractV function


## -description


Refracts an incident 3D vector across a 3D normal vector.


## -parameters




### -param Incident [in]

3D incident vector to refract.


### -param Normal [in]

3D normal vector to refract the incident vector through.


### -param RefractionIndex [in]

3D vector whose x, y, and z-components are equal to the index of refraction.


## -returns



Returns the refracted incident vector. If the refraction index and the angle between the incident vector and the normal
       are such that the result is a total internal reflection, the function will return a vector of the form &lt;
       0.0f, 0.0f, 0.0f, undefined &gt;.




## -remarks



This function is identical to
   <a href="https://msdn.microsoft.com/035b05dc-af61-4a7d-a48f-a2ad19f4389a">XMVector3Refract</a> except that the
   <i>RefractionIndex</i> is supplied using a 3D vector instead of a <b>float</b> value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/f2cee697-b4ec-5e4d-a87b-622c9fb7997c">DirectXMath Library 3D Vector Geometric Functions</a>



<a href="https://msdn.microsoft.com/d92d2d21-dbd0-4902-ad52-db4ba1c96ae6">XMVector2Refract</a>
 

 

