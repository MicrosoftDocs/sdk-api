---
UID: NF:directxcollision.BoundingFrustum.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
title: BoundingFrustum::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)
author: windows-sdk-content
description: Tests whether the BoundingFrustum contains the specified triangle.
old-location: dxmath\boundingfrustum_contains_2.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxmath.BoundingFrustum.Contains(XMVECTOR,XMVECTOR,XMVECTOR)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BoundingFrustum interface [DirectX Math Support APIs],Contains method, BoundingFrustum.Contains, BoundingFrustum.Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), BoundingFrustum.Contains(XMVECTOR,XMVECTOR,XMVECTOR), BoundingFrustum::Contains, BoundingFrustum::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingFrustum interface, dxmath.boundingfrustum_contains_2
ms.topic: method
f1_keywords: ["directxcollision/BoundingFrustum.Contains"]
req.header: directxcollision.h
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
req.namespace: 
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
 - DirectXCollision.h
api_name:
 - BoundingFrustum.Contains
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingFrustum::Contains(FXMVECTOR,FXMVECTOR,FXMVECTOR)


## -description


Tests whether the <a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a> contains the specified triangle.


## -parameters




### -param V0 [in]

A corner of the triangle.


### -param V1 [in]

A corner of the triangle.


### -param V2 [in]

A corner of the triangle.


## -returns



A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> value indicating whether the triangle is contained in the <a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a>



<a href="https://msdn.microsoft.com/b75bff54-710e-4474-9953-444970a78853">Contains</a>



<b>Reference</b>
 

 

