---
UID: NF:d2d1.ID2D1Geometry.Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
author: windows-sdk-content
description: Widens the geometry by the specified stroke and writes the result to an ID2D1SimplifiedGeometrySink after it has been transformed by the specified matrix and flattened using the specified tolerance.
old-location: direct2d\ID2D1Geometry_Widen_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: direct2d
ms.assetid: f0adc3fa-be9e-489e-9de3-465daa0f41c5
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Widen method, ID2D1Geometry.Widen, ID2D1Geometry.Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Widen, ID2D1Geometry::Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), Widen, Widen method [Direct2D], Widen method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Widen, direct2d.ID2D1Geometry_Widen_FLOAT_ptr_ID2D1StrokeStyle_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry.Widen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::Widen(FLOAT,ID2D1StrokeStyle,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)


## -description


Widens the geometry by the specified stroke and writes the result to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a> after it has been transformed by the specified matrix and flattened using the specified tolerance.


## -parameters




### -param strokeWidth

Type: <b>FLOAT</b>

The amount by which to widen the geometry.


### -param strokeStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a>*</b>

The style of stroke to apply to the geometry, or <b>NULL</b>.


### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry after widening it, or <b>NULL</b>.


### -param geometrySink [in]

Type: <b><a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a> to which the widened geometry is appended.


#### - flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

