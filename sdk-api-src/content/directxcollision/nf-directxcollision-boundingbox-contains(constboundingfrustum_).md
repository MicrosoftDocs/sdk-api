---
UID: NF:directxcollision.BoundingBox.Contains(const BoundingFrustum &)
title: BoundingBox::Contains(const BoundingFrustum &)
description: Tests whether the BoundingBox contains the specified BoundingFrustum.helpviewer_keywords: ["BoundingBox interface [DirectX Math Support APIs]","Contains method","BoundingBox.Contains","BoundingBox.Contains(const BoundingFrustum &)","BoundingBox.Contains(const BoundingFrustum&)","BoundingBox::Contains","BoundingBox::Contains(const BoundingFrustum &)","Contains","Contains method [DirectX Math Support APIs]","Contains method [DirectX Math Support APIs]","BoundingBox interface","dxmath.boundingbox_contains_1"]
old-location: dxmath\boundingbox_contains_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.Contains(BoundingFrustum)
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],Contains method, BoundingBox.Contains, BoundingBox.Contains(const BoundingFrustum &), BoundingBox.Contains(const BoundingFrustum&), BoundingBox::Contains, BoundingBox::Contains(const BoundingFrustum &), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_contains_1
f1_keywords:
- directxcollision/BoundingBox.Contains
dev_langs:
- c++
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
- BoundingBox.Contains
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingBox::Contains(const BoundingFrustum &)


## -description


Tests whether the [BoundingBox](/windows/win32/api/directxcollision/ns-directxcollision-boundingbox) contains the specified [BoundingFrustum](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum).


## -parameters




### -param fr [in, ref]

The [BoundingFrustum](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) to test against.


## -returns



A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> value indicating whether the [BoundingFrustum](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum) is contained in the [BoundingBox](/windows/win32/api/directxcollision/ns-directxcollision-boundingbox).




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




[BoundingBox](/windows/win32/api/directxcollision/ns-directxcollision-boundingbox)



<a href="https://msdn.microsoft.com/876c7764-9378-48e5-812c-3646930900c5">Contains</a>



<b>Reference</b>
 

 

