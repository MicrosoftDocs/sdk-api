---
UID: NF:d2d1.ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1SimplifiedGeometrySink) (d2d1.h)
description: Computes the outline of the geometry and writes the result to an ID2D1SimplifiedGeometrySink.helpviewer_keywords: ["ID2D1Geometry interface [Direct2D]","Outline method","ID2D1Geometry.Outline","ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F &","FLOAT","ID2D1SimplifiedGeometrySink)","ID2D1Geometry::Outline","ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F &","FLOAT","ID2D1SimplifiedGeometrySink)","Outline","Outline method [Direct2D]","Outline method [Direct2D]","ID2D1Geometry interface","d2d1/ID2D1Geometry::Outline","direct2d.ID2D1Geometry_Outline_ref_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1Geometry_Outline_ref_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: 28ca0da9-f510-44b3-a10a-7dbae8b24c54
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Outline method, ID2D1Geometry.Outline, ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Outline, ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1SimplifiedGeometrySink), Outline, Outline method [Direct2D], Outline method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Outline, direct2d.ID2D1Geometry_Outline_ref_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink
f1_keywords:
- d2d1/ID2D1Geometry.Outline
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
- ID2D1Geometry.Outline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F &,FLOAT,ID2D1SimplifiedGeometrySink)


## -description


Computes the outline of the geometry and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.


## -parameters




### -param worldTransform [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a></b>

The transform to apply to the geometry outline.


### -param flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution. 



### -param geometrySink [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> to which the geometry transformed outline is appended. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

