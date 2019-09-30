---
UID: NF:gdipluspath.GraphicsPath.AddEllipse(IN const Rect &)
title: GraphicsPath::AddEllipse(IN const Rect &) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddEllipse method adds an ellipse to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddEllipse_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddellipsemethods\addellipse.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddEllipse, AddEllipse method [GDI+], AddEllipse method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddEllipse method, GraphicsPath.AddEllipse, GraphicsPath.AddEllipse(IN const Rect &), GraphicsPath.AddEllipse(const Rect&), GraphicsPath::AddEllipse, GraphicsPath::AddEllipse(IN const Rect &), _gdiplus_CLASS_GraphicsPath_AddEllipse_Rect_rect_, gdiplus._gdiplus_CLASS_GraphicsPath_AddEllipse_Rect_rect_
ms.topic: method
f1_keywords: 
 - "gdipluspath/GraphicsPath.AddEllipse"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddEllipse
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::AddEllipse(IN const Rect &)


## -description


The <b>GraphicsPath::AddEllipse</b> method adds an ellipse to this path.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that bounds the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



A <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object stores an ellipse as a sequence of four connected Bézier splines. The <b>GraphicsPath</b> object does not store the upper-left corner, width, and height of the ellipse's bounding rectangle.


#### Examples



The following example creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds an ellipse to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddEllipse(HDC hdc)
{
   Graphics graphics(hdc); 
   Rect rect(20, 20, 200, 100);

   GraphicsPath path;
   path.AddEllipse(rect);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inconstrect__inreal_inreal)">AddArc Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inconstrect_)">AddEllipse Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-ellipses-and-arcs-about">Ellipses and Arcs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>
 

 

