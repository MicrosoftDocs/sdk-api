---
UID: NF:directxmath.XMVector2RefractV
title: XMVector2RefractV function
author: windows-sdk-content
description: Refracts an incident 2D vector across a 2D normal vector.
old-location: dxmath\xmvector2refractv.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.geometric.XMVector2RefractV(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMVector2RefractV, XMVector2RefractV, XMVector2RefractV method [DirectX Math Support APIs], dxmath.xmvector2refractv
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
 - XMVector2RefractV
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMVector2RefractV
: 
---

# XMVector2RefractV function


## -description


Refracts an incident 2D vector across a 2D normal vector.


## -parameters




### -param Incident [in]

2D incident vector to refract.


### -param Normal [in]

2D normal vector to refract the incident vector through.


### -param RefractionIndex [in]

2D vector whose x and y-components are both equal to the index of refraction.


## -returns



Returns the refracted incident vector. If the refraction index and the angle between the incident vector and the normal are such that the result is a total internal reflection, the function will return a vector of the form &lt; 0.0f, 0.0f, undefined, undefined &gt;.




## -remarks



This function is identical to <a href="https://msdn.microsoft.com/d92d2d21-dbd0-4902-ad52-db4ba1c96ae6">XMVector2Refract</a> except that the <i>RefractionIndex</i> is supplied using a 2D vector instead of a <b>float</b> value.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/a17cdad7-4fbe-bf83-472f-1b99603b7fec">DirectXMath Library 2D Vector Geometric Functions</a>



<a href="https://msdn.microsoft.com/d92d2d21-dbd0-4902-ad52-db4ba1c96ae6">XMVector2Refract</a>
 

 

