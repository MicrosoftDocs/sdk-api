---
UID: NF:d2d1.ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink)
title: ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink)
author: windows-sdk-content
description: Computes the outline of the geometry and writes the result to an ID2D1SimplifiedGeometrySink.
old-location: direct2d\ID2D1Geometry_Outline_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink.htm
tech.root: direct2d
ms.assetid: ee5edc52-eff7-4e7e-8f77-020e7967e6f5
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1Geometry interface [Direct2D],Outline method, ID2D1Geometry.Outline, ID2D1Geometry.Outline(const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink), ID2D1Geometry::Outline, ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink), Outline, Outline method [Direct2D], Outline method [Direct2D],ID2D1Geometry interface, d2d1/ID2D1Geometry::Outline, direct2d.ID2D1Geometry_Outline_ptr_D2D_MATRIX_3X2_F_FLOAT_ptr_ID2D1SimplifiedGeometrySink
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
 - ID2D1Geometry.Outline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Geometry::Outline(const D2D1_MATRIX_3X2_F,FLOAT,ID2D1SimplifiedGeometrySink)


## -description


Computes the outline of the geometry and writes the result to an <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>.


## -parameters




### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The transform to apply to the geometry outline, or <b>NULL</b>.



### -param flatteningTolerance

Type: <b>FLOAT</b>

The maximum error allowed when constructing a polygonal approximation of the geometry. No point in the polygonal representation will diverge from the original geometry by more than the flattening tolerance. Smaller values produce more accurate results but cause slower execution. 



### -param geometrySink [in]

Type: <b><a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a>*</b>

The <a href="https://msdn.microsoft.com/cf877a25-7b9f-4db0-ac53-b4a350795a86">ID2D1SimplifiedGeometrySink</a> to which the geometry's transformed outline is appended. 


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/138b8835-2fd1-4e9e-b607-a3666f2275bd">Outline</a> method allows the caller to produce a geometry with an equivalent fill to the input geometry, with the following additional properties:
	

<ul>
<li>The output geometry contains no transverse intersections; that is, segments may touch, but they never cross.</li>
<li>The outermost figures in the output geometry are all oriented counterclockwise.
	</li>
<li>The output geometry is fill-mode invariant; that is, the fill of the geometry does not depend on the choice of the fill mode.

 For more information about the fill mode, see <a href="https://msdn.microsoft.com/f1a14447-39fa-4a48-9516-ff5b03abc3a6">D2D1_FILL_MODE</a>.</li>
</ul>
Additionally, the 
	<a href="https://msdn.microsoft.com/138b8835-2fd1-4e9e-b607-a3666f2275bd">Outline</a> method can be useful in removing redundant portions of said geometries to simplify complex geometries. It can also be useful in combination with <a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a> to create unions among several geometries simultaneously.





## -see-also




<a href="https://msdn.microsoft.com/be4ab801-64f6-48f9-8f62-d0492cc438b1">ID2D1Geometry</a>
 

 

