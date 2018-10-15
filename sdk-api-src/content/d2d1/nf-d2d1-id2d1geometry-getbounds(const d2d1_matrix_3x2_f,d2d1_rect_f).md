---
UID: NF:d2d1.ID2D1Geometry.GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F)
title: ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F)
author: windows-sdk-content
description: Retrieves the bounds of the geometry.
old-location: direct2d\ID2D1Geometry_GetBounds_ptr_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F.htm
tech.root: direct2d
ms.assetid: 5dc79a72-60d5-4a6d-94e6-d8a476d01c19
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetBounds, GetBounds method [Direct2D], GetBounds method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],GetBounds method, ID2D1Geometry.GetBounds, ID2D1Geometry.GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F), ID2D1Geometry::GetBounds, ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F), d2d1/ID2D1Geometry::GetBounds, direct2d.ID2D1Geometry_GetBounds_ptr_D2D_MATRIX_3X2_F_ptr_D2D_RECT_F
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Geometry.GetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::GetBounds(const D2D1_MATRIX_3X2_F,D2D1_RECT_F)


## -description


Retrieves the bounds of the geometry.


## -parameters




### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to this geometry before calculating its bounds, or <b>NULL</b>.



### -param bounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

When this method returns, contains the bounds of this geometry. If the bounds are empty, this parameter will be a rect where <i>bounds.left</i> &gt; <i>bounds.right</i>. You must allocate storage for this parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

