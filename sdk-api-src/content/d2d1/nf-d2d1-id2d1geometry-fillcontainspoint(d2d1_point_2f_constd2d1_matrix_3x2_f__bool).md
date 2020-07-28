---
UID: NF:d2d1.ID2D1Geometry.FillContainsPoint(D2D1_POINT_2F,constD2D1_MATRIX_3X2_F&,BOOL)
title: ID2D1Geometry::FillContainsPoint(D2D1_POINT_2F,const D2D1_MATRIX_3X2_F &,BOOL) (d2d1.h)
description: Indicates whether the area filled by the geometry would contain the specified point.
helpviewer_keywords: ["FillContainsPoint","FillContainsPoint method [Direct2D]","FillContainsPoint method [Direct2D]","ID2D1Geometry interface","ID2D1Geometry interface [Direct2D]","FillContainsPoint method","ID2D1Geometry.FillContainsPoint","ID2D1Geometry.FillContainsPoint(D2D1_POINT_2F","const D2D1_MATRIX_3X2_F &","BOOL)","ID2D1Geometry::FillContainsPoint","ID2D1Geometry::FillContainsPoint(D2D1_POINT_2F","const D2D1_MATRIX_3X2_F &","BOOL)","d2d1/ID2D1Geometry::FillContainsPoint","direct2d.ID2D1Geometry_FillContainsPoint_D2D_POINT_2F_ref_D2D_MATRIX_3X2_F_ptr_BOOL"]
old-location: direct2d\ID2D1Geometry_FillContainsPoint_D2D_POINT_2F_ref_D2D_MATRIX_3X2_F_ptr_BOOL.htm
tech.root: Direct2D
ms.assetid: d78efac3-2751-4a7e-8682-59b1a36c28cd
ms.date: 12/05/2018
ms.keywords: FillContainsPoint, FillContainsPoint method [Direct2D], FillContainsPoint method [Direct2D],ID2D1Geometry interface, ID2D1Geometry interface [Direct2D],FillContainsPoint method, ID2D1Geometry.FillContainsPoint, ID2D1Geometry.FillContainsPoint(D2D1_POINT_2F,const D2D1_MATRIX_3X2_F &,BOOL), ID2D1Geometry::FillContainsPoint, ID2D1Geometry::FillContainsPoint(D2D1_POINT_2F,const D2D1_MATRIX_3X2_F &,BOOL), d2d1/ID2D1Geometry::FillContainsPoint, direct2d.ID2D1Geometry_FillContainsPoint_D2D_POINT_2F_ref_D2D_MATRIX_3X2_F_ptr_BOOL
f1_keywords:
- d2d1/ID2D1Geometry.FillContainsPoint
dev_langs:
- c++
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
- ID2D1Geometry.FillContainsPoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry::FillContainsPoint(D2D1_POINT_2F,const D2D1_MATRIX_3X2_F &,BOOL)


## -description


Indicates whether the area filled by the geometry would contain the specified point.


## -parameters




### -param point

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The point to test.



### -param worldTransform [ref]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transform to apply to the geometry prior to testing for containment.


### -param contains [out]

Type: <b>BOOL*</b>

When this method returns, contains a bool value that is true if the area filled by the geometry contains <i>point</i>; otherwise, false.
You must allocate storage for this parameter.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.




## -see-also




<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

