---
UID: NF:gdipluspath.GraphicsPath.AddPath
title: GraphicsPath::AddPath
author: windows-sdk-content
description: The GraphicsPath::AddPath method adds a path to this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\addpath.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AddPath, AddPath method [GDI+], AddPath method [GDI+],GraphicsPath class, FALSE, GraphicsPath class [GDI+],AddPath method, GraphicsPath.AddPath, GraphicsPath::AddPath, TRUE, _gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_, gdiplus._gdiplus_CLASS_GraphicsPath_AddPath_addingPath_connect_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.AddPath
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddPath


## -description


The <b>GraphicsPath::AddPath</b> method adds a path to this path.


## -parameters




### -param addingPath [in]

Type: <b>const <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>*</b>

Pointer to the path to be added. 


### -param connect [in]

Type: <b>BOOL</b>

<b>BOOL</b> value that specifies whether the first figure in the added path is part of the last figure in this path.



#### TRUE

Specifies that (if possible) the first figure in the added path is part of the last figure in this path.



#### FALSE

Specifies that the first figure in the added path is separate from the last figure in this path.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



Even if the value of the <i>connect</i> parameter is <b>TRUE</b>, this method might not be able to make the first figure of the added path part of the last figure of this path. If either of those figures is closed, then they must remain separate figures.


#### Examples



The following example creates two <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> objects: <i>path1</i> and <i>path2</i>. The code adds an open figure consisting of an arc and a Bézier spline to each path. The code calls the <b>GraphicsPath::AddPath</b> method of <i>path1</i> to add <i>path2</i> to <i>path1</i>. The second argument is <b>TRUE</b>, which specifies that all four items (two arcs and two Bézier splines) belong to the same figure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID AddPathExample(HDC hdc)
{
   Graphics graphics(hdc);

   GraphicsPath path1;
   path1.AddArc(10, 10, 50, 20, 0.0f, 150.0f);
   path1.AddBezier(10, 50, 60, 50, 10, 80, 60, 80);
   
   GraphicsPath path2;
   path2.AddArc(10, 110, 50, 20, 0.0f, 150.0f);
   path2.AddBezier(10, 150, 60, 150, 10, 180, 60, 180);
 
   path1.AddPath(&amp;path2, TRUE);

   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;pen, &amp;path1);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/39074cd8-267d-485a-8175-d0a25dcf9097">AddEllipse Methods</a>



<a href="https://msdn.microsoft.com/b86c87c0-7d6b-4e9d-b276-a98ac9a33772">AddRectangle Methods</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

