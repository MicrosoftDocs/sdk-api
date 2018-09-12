---
UID: NF:gdipluspath.GraphicsPath.Reverse
title: GraphicsPath::Reverse
author: windows-sdk-content
description: The GraphicsPath::Reverse method reverses the order of the points that define this path's lines and curves.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Reverse_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\reverse.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GraphicsPath class [GDI+],Reverse method, GraphicsPath.Reverse, GraphicsPath::Reverse, Reverse, Reverse method [GDI+], Reverse method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Reverse_, gdiplus._gdiplus_CLASS_GraphicsPath_Reverse_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GraphicsPath.Reverse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::Reverse


## -description


The <b>GraphicsPath::Reverse</b> method reverses the order of the points that define this path's lines and curves.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration. 

This method reverses the order of the elements in the array of points and in the array of types.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object <i>path</i>, adds two lines to <i>path</i>, calls the <b>Reverse</b> method, and then draws <i>path</i>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID ReverseExample(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsPath path;

   // Set up and call Reverse.
   Point pts[] = {Point(10, 60),
                  Point(50, 110),
                  Point(90, 60)};
   path.AddLines(pts, 3);
   path.Reverse();

   // Draw the path.
   graphics.DrawPath(&amp;Pen(Color(128, 255, 0, 0), 2), &amp;path);
}
 </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535544(v=VS.85).aspx">AddLines Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535534(v=VS.85).aspx">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535535(v=VS.85).aspx">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>
 

 

