---
UID: NF:directxcollision.BoundingBox.Contains(const BoundingFrustum &)
title: BoundingBox::Contains(const BoundingFrustum &)
author: windows-sdk-content
description: Tests whether the BoundingBox contains the specified BoundingFrustum.
old-location: dxmath\boundingbox_contains_1.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.directxcollision.BoundingBox.Contains(BoundingFrustum)
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BoundingBox interface [DirectX Math Support APIs],Contains method, BoundingBox.Contains, BoundingBox.Contains(const BoundingFrustum &), BoundingBox.Contains(const BoundingFrustum&), BoundingBox::Contains, BoundingBox::Contains(const BoundingFrustum &), Contains, Contains method [DirectX Math Support APIs], Contains method [DirectX Math Support APIs],BoundingBox interface, dxmath.boundingbox_contains_1
ms.topic: method
f1_keywords: ["directxcollision/BoundingBox.Contains"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BoundingBox::Contains(const BoundingFrustum &)


## -description


Tests whether the <a href="https://msdn.microsoft.com/8dac1c63-2eb6-4ad2-8495-593c4927391f">BoundingBox</a> contains the specified <a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a>.


## -parameters




### -param fr [in, ref]

The <a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a> to test against.


## -returns



A <a href="https://msdn.microsoft.com/edc456b5-2d68-4d4e-953b-6081ad7f663c">ContainmentType</a> value indicating whether the <a href="https://msdn.microsoft.com/C0C961B6-6F6B-443B-B02F-2601E158F51B">BoundingFrustum</a> is contained in the <a href="https://msdn.microsoft.com/8dac1c63-2eb6-4ad2-8495-593c4927391f">BoundingBox</a>.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/8dac1c63-2eb6-4ad2-8495-593c4927391f">BoundingBox</a>



<a href="https://msdn.microsoft.com/876c7764-9378-48e5-812c-3646930900c5">Contains</a>



<b>Reference</b>
 

 

