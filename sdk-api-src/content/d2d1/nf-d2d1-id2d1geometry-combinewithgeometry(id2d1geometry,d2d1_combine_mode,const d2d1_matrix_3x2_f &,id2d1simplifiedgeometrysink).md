---
UID: NF:d2d1.ID2D1Geometry.CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)
author: windows-sdk-content
description: Combines this geometry with the specified geometry and stores the result in an ID2D1SimplifiedGeometrySink.
old-location: direct2d\ID2D1Geometry_CombineWithGeometry_ptr_ID2D1Geometry_D2D1_COMBINE_MODE_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: direct2d
ms.assetid: 8fc4528a-7643-47ad-ba4d-5f83733e9935
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CombineWithGeometry, CombineWithGeometry method [Direct2D], CombineWithGeometry method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],CombineWithGeometry method, ID2D1Geometry.CombineWithGeometry, ID2D1Geometry.CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), ID2D1Geometry::CombineWithGeometry, ID2D1Geometry::CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink), d2d1/ID2D1Geometry::CombineWithGeometry, direct2d.ID2D1Geometry_CombineWithGeometry_ptr_ID2D1Geometry_D2D1_COMBINE_MODE_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry.CombineWithGeometry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::CombineWithGeometry(ID2D1Geometry,D2D1_COMBINE_MODE,const D2D1_MATRIX_3X2_F &,ID2D1SimplifiedGeometrySink)


## -description


Combines this geometry with the specified geometry and stores the result in an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>. 




## -parameters




### -param inputGeometry [in]

Type: <b><a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>*</b>

The geometry to combine with this instance.



### -param combineMode

Type: <b><a href="https://msdn.microsoft.com/7526379a-5f57-4a9f-b85d-415f131528e2">D2D1_COMBINE_MODE</a></b>

The type of combine operation to perform.



### -param inputGeometryTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to <i>inputGeometry</i> before combining, or <b>NULL</b>.



### -param geometrySink [in]

Type: <b><a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>*</b>

The result of the combine operation.


#### - flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution.



## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

