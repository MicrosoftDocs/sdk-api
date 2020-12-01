---
UID: NF:gdipluspath.GraphicsPath.AddPath
title: GraphicsPath::AddPath (gdipluspath.h)
description: The GraphicsPath::AddPath method adds a path to this path.
helpviewer_keywords: ["AddPath","AddPath method [GDI+]","AddPath method [GDI+]","GraphicsPath class","FALSE","GraphicsPath class [GDI+]","AddPath method","GraphicsPath.AddPath","GraphicsPath::AddPath","TRUE","_gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_","gdiplus._gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\addpath.htm
ms.date: 12/05/2018
ms.keywords: AddPath, AddPath method [GDI+], AddPath method [GDI+],GraphicsPath class, FALSE, GraphicsPath class [GDI+],AddPath method, GraphicsPath.AddPath, GraphicsPath::AddPath, TRUE, _gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_, gdiplus._gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_
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
 - GraphicsPath::AddPath
 - gdipluspath/GraphicsPath::AddPath
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
 - GraphicsPath.AddPath
---

# GraphicsPath::AddPath


## -description

The <b>GraphicsPath::AddPath</b> method adds a path to this path.

## -parameters

### -param addingPath [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to the path to be added.

### -param connect [in]

Type: <b>BOOL</b>

<b>BOOL</b> value that specifies whether the first figure in the added path is part of the last figure in this path.



#### TRUE

Specifies that (if possible) the first figure in the added path is part of the last figure in this path.



#### FALSE

Specifies that the first figure in the added path is separate from the last figure in this path.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Even if the value of the <i>connect</i> parameter is <b>TRUE</b>, this method might not be able to make the first figure of the added path part of the last figure of this path. If either of those figures is closed, then they must remain separate figures.


#### Examples



The following example creates two <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> objects: <i>path1</i> and <i>path2</i>. The code adds an open figure consisting of an arc and a Bézier spline to each path. The code calls the <b>GraphicsPath::AddPath</b> method of <i>path1</i> to add <i>path2</i> to <i>path1</i>. The second argument is <b>TRUE</b>, which specifies that all four items (two arcs and two Bézier splines) belong to the same figure.


```cpp
VOID AddPathExample(HDC hdc)
{
   Graphics graphics(hdc);

   GraphicsPath path1;
   path1.AddArc(10, 10, 50, 20, 0.0f, 150.0f);
   path1.AddBezier(10, 50, 60, 50, 10, 80, 60, 80);
   
   GraphicsPath path2;
   path2.AddArc(10, 110, 50, 20, 0.0f, 150.0f);
   path2.AddBezier(10, 150, 60, 150, 10, 180, 60, 180);
 
   path1.AddPath(&path2, TRUE);

   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&pen, &path1);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inconstrect_)">AddEllipse Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrect_)">AddRectangle Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>