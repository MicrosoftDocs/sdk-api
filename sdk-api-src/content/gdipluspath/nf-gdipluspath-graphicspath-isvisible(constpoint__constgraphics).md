---
UID: NF:gdipluspath.GraphicsPath.IsVisible(constPoint&,constGraphics)
title: GraphicsPath::IsVisible(IN const Point &,IN const Graphics) (gdipluspath.h)
description: The GraphicsPath::IsVisible method determines whether a specified point lies in the area that is filled when this path is filled by a specified Graphics object. (overload 1/2)
helpviewer_keywords: ["GraphicsPath class [GDI+]","IsVisible method","GraphicsPath.IsVisible","GraphicsPath.IsVisible(IN const Point &","IN const Graphics)","GraphicsPath.IsVisible(const Point&","const Graphics*)","GraphicsPath::IsVisible","GraphicsPath::IsVisible(IN const Point &","IN const Graphics)","IsVisible","IsVisible method [GDI+]","IsVisible method [GDI+]","GraphicsPath class","_gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_","gdiplus._gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisvisiblemethods\isvisible_90pointamppoint_graphicsg.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPath class [GDI+],IsVisible method, GraphicsPath.IsVisible, GraphicsPath.IsVisible(IN const Point &,IN const Graphics), GraphicsPath.IsVisible(const Point&,const Graphics*), GraphicsPath::IsVisible, GraphicsPath::IsVisible(IN const Point &,IN const Graphics), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GraphicsPath::IsVisible
 - gdipluspath/GraphicsPath::IsVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.IsVisible
---

# GraphicsPath::IsVisible(IN const Point &,IN const Graphics)


## -description

The <b>GraphicsPath::IsVisible</b> method determines whether a specified point lies in the area that is filled when this path is filled by a specified <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object.

## -parameters

### -param point [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to the point to be tested.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Optional. Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

If the test point lies in the interior of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isoutlinevisible(inconstpoint__inconstpen_inconstgraphics)">IsOutlineVisible Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-isvisible(inconstpoint__inconstgraphics)">IsVisible Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
