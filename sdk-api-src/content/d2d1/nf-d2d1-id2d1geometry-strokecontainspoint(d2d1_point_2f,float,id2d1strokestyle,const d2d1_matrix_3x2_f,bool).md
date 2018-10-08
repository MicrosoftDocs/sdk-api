---
UID: NF:d2d1.ID2D1Geometry.StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F,BOOL)
title: ID2D1Geometry::StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F,BOOL)
author: windows-sdk-content
description: Determines whether the geometry's stroke contains the specified point given the specified stroke thickness, style, and transform.
old-location: direct2d\ID2D1Geometry_StrokeContainsPoint_D2D_POINT_2F_FLOAT_ptr_ID2D1StrokeStyle_ref_D2D_MATRIX_3X2_F_ptr_BOOL.htm
tech.root: Direct2D
ms.assetid: 51cc93a9-bd07-43ef-869a-758a04a3bec5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],StrokeContainsPoint method, ID2D1Geometry.StrokeContainsPoint, ID2D1Geometry.StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F,BOOL), ID2D1Geometry::StrokeContainsPoint, ID2D1Geometry::StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F,BOOL), StrokeContainsPoint, StrokeContainsPoint method [Direct2D], StrokeContainsPoint method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::StrokeContainsPoint, direct2d.ID2D1Geometry_StrokeContainsPoint_D2D_POINT_2F_FLOAT_ptr_ID2D1StrokeStyle_ref_D2D_MATRIX_3X2_F_ptr_BOOL
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
 - ID2D1Geometry.StrokeContainsPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::StrokeContainsPoint(D2D1_POINT_2F,FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F,BOOL)


## -description


Determines whether the geometry's stroke contains the specified point given the specified stroke thickness, style, and transform.




## -parameters




### -param point

Type: <b><a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The point to test for containment.



### -param strokeWidth

Type: <b>FLOAT</b>

The thickness of the stroke to apply.



### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply.


### -param worldTransform [ref]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a></b>

The transform to apply to the stroked geometry. 



### -param contains [out]

Type: <b>BOOL*</b>

When this method returns, contains a boolean value set to true if the geometry's stroke contains the specified point; otherwise, false. You must allocate storage for this parameter.



## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

