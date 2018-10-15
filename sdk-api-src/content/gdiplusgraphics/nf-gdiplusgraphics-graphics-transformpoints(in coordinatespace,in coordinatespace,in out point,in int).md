---
UID: NF:gdiplusgraphics.Graphics.TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)
title: Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)
author: windows-sdk-content
description: The Graphics::TransformPoints method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\transformpoints.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Graphics class [GDI+],TransformPoints method, Graphics.TransformPoints, Graphics.TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT), Graphics::TransformPoints, Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT), TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_, gdiplus._gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.TransformPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)


## -description


The <b>Graphics::TransformPoints</b> method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param destSpace [in]

Type: <b><a href="https://msdn.microsoft.com/8e2bd6cd-3a8d-46f8-b669-868cf46f3a82">CoordinateSpace</a></b>

Element of the <a href="https://msdn.microsoft.com/8e2bd6cd-3a8d-46f8-b669-868cf46f3a82">CoordinateSpace</a> enumeration that specifies the destination coordinate space. 


### -param srcSpace [in]

Type: <b><a href="https://msdn.microsoft.com/8e2bd6cd-3a8d-46f8-b669-868cf46f3a82">CoordinateSpace</a></b>

Element of the <a href="https://msdn.microsoft.com/8e2bd6cd-3a8d-46f8-b669-868cf46f3a82">CoordinateSpace</a> enumeration that specifies the source coordinate space. 


### -param pts [in, out]

Type: <b><a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array that, on input, holds the points to be converted and, on output, holds the converted points. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>pts</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The world transformation converts points from the world coordinate space to the page coordinate space. The page transformation converts points from the page coordinate space to the device coordinate space. For more information about coordinate spaces, see <a href="https://msdn.microsoft.com/eb20f5e9-25f5-4f27-8ea5-83f6819425ed">Types of Coordinate Systems</a>.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object and sets its world transformation to a translation 40 units right and 30 units down. Then the code creates an array of points and passes the address of that array to the <b>Graphics::TransformPoints</b> method of the same <b>Graphics</b> object. The points in the array are transformed by the world transformation of the <b>Graphics</b> object. The code calls the <a href="https://msdn.microsoft.com/edaaedfd-6b45-45e6-b23c-df4304420177">Graphics::DrawLine</a> method twice: once to connect the two points before the transformation and once to connect the two points after the transformation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_TransformPoints(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   // Create an array of two Point objects.
   Point points[2] = {Point(0, 0), Point(100, 50)};

   // Draw a line that connects the two points.
   // No transformation has been performed yet.
   graphics.DrawLine(&amp;pen, points[0], points[1]);

   // Set the world transformation of the Graphics object.
   graphics.TranslateTransform(40.0f, 30.0f);

   // Transform the points in the array from world to page coordinates.
   graphics.TransformPoints(
      CoordinateSpacePage, 
      CoordinateSpaceWorld, 
      points, 
      2);

   // It is the world transformation that takes points from world
   // space to page space. Because the world transformation is a
   // translation 40 to the right and 30 down, the
   // points in the array are now (40, 30) and (140, 80).

   // Draw a line that connects the transformed points.
   graphics.ResetTransform();
   graphics.DrawLine(&amp;pen, points[0], points[1]);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/f5f1a7bb-4f17-4865-b26e-8672ae78c3a7">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/46f90c3e-ed70-40ba-a8e8-1b1d3276862d">Graphics::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/10357224-cfbd-4d02-af94-93cdff80d466">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/554cd11e-9b22-48c5-a823-bd29f879fba7">Graphics::RotateTransform</a>



<a href="https://msdn.microsoft.com/040bfd10-1a2b-4277-9d27-0919d9efe371">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/99b51fb7-b1de-421f-9743-bf6a5ec758ef">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>



<a href="https://msdn.microsoft.com/eb20f5e9-25f5-4f27-8ea5-83f6819425ed">Types of Coordinate Systems</a>
 

 

