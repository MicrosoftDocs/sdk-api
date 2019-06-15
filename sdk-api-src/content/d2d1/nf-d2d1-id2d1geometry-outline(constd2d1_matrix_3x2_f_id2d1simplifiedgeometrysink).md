---
UID: NF:d2d1.ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink) (d2d1.h)
author: windows-sdk-content
description: Computes the outline of the geometry and writes the result to an ID2D1SimplifiedGeometrySink.
old-location: direct2d\ID2D1Geometry_Outline_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: 10ab30b9-6141-4b4f-a3e7-9aa690043381
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Outline method, ID2D1Geometry.Outline, ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Outline, ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink), Outline, Outline method [Direct2D], Outline method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Outline, direct2d.ID2D1Geometry_Outline_ptr_D2D_MATRIX_3X2_F_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry.Outline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,ID2D1SimplifiedGeometrySink)


## -description


Computes the outline of the geometry and writes the result to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>.


## -parameters




### -param worldTransform [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry outline, or <b>NULL</b>.


### -param geometrySink [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a> to which the geometry's transformed outline is appended. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)">Outline</a> method allows the caller to produce a geometry with an equivalent fill to the input geometry, with the following additional properties:
	

<ul>
<li>The output geometry contains no transverse intersections; that is, segments may touch, but they never cross.</li>
<li>The outermost figures in the output geometry are all oriented counterclockwise.
	</li>
<li>The output geometry is fill-mode invariant; that is, the fill of the geometry does not depend on the choice of the fill mode.

 For more information about the fill mode, see <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode">D2D1_FILL_MODE</a>.</li>
</ul>
Additionally, the 
	<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)">Outline</a> method can be useful in removing redundant portions of said geometries to simplify complex geometries. It can also be useful in combination with <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a> to create unions among several geometries simultaneously.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometry">ID2D1Geometry</a>
 

 

