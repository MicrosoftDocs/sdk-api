---
UID: NF:gdipluspath.GraphicsPath.AddEllipse(IN INT,IN INT,IN INT,IN INT)
title: GraphicsPath::AddEllipse(IN INT,IN INT,IN INT,IN INT) (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::AddEllipse method adds an ellipse to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddEllipse_INT_x_INT_y_INT_width_INT_height_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddellipsemethods\addellipse_29intx_inty_intwidth_intheight.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddEllipse, AddEllipse method [GDI+], AddEllipse method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddEllipse method, GraphicsPath.AddEllipse, GraphicsPath.AddEllipse(IN INT,IN INT,IN INT,IN INT), GraphicsPath.AddEllipse(INT,INT,INT,INT), GraphicsPath::AddEllipse, GraphicsPath::AddEllipse(IN INT,IN INT,IN INT,IN INT), _gdiplus_CLASS_GraphicsPath_AddEllipse_INT_x_INT_y_INT_width_INT_height_, gdiplus._gdiplus_CLASS_GraphicsPath_AddEllipse_INT_x_INT_y_INT_width_INT_height_
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GraphicsPath::AddEllipse(IN INT,IN INT,IN INT,IN INT)


## -description


The <b>GraphicsPath::AddEllipse</b> method adds an ellipse to this path.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the upper-left corner of the bounding rectangle for the ellipse. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the upper-left corner of the bounding rectangle for the ellipse. 


### -param width [in]

Type: <b>INT</b>

Integer that specifies the width of the bounding rectangle for the ellipse. 


### -param height [in]

Type: <b>INT</b>

Integer that specifies the height of the bounding rectangle for the ellipse. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object stores an ellipse as a sequence of four connected Bézier splines. The <b>GraphicsPath</b> object does not store the upper-left corner, width, and height of the ellipse's bounding rectangle.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object <i>path</i>, adds an ellipse to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddEllipse(HDC hdc)
{
   Graphics graphics(hdc); 

   GraphicsPath path;
   path.AddEllipse(20, 20, 200, 100);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535537(v=VS.85).aspx">AddArc Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535542(v=VS.85).aspx">AddEllipse Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

