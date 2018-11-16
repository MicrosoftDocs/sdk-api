---
UID: NF:gdiplusbrush.LinearGradientBrush.SetTransform
title: LinearGradientBrush::SetTransform
author: windows-sdk-content
description: The LinearGradientBrush::SetTransform method sets the transformation matrix of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\settransform_65matrix.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LinearGradientBrush class [GDI+],SetTransform method, LinearGradientBrush.SetTransform, LinearGradientBrush::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
 - LinearGradientBrush.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusbrush.h
: 
- LinearGradientBrush.SetTransform
: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::SetTransform


## -description


The <b>LinearGradientBrush::SetTransform</b> method sets the transformation matrix of this linear gradient brush.


## -parameters




### -param matrix [in]

Type: <b>const Matrix*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object has a rectangle that specifies the starting and ending boundaries of the gradient and a mode or angle that affects the direction. If the brush's transformation matrix is set to represent any transformation other than the identity, then the boundaries and direction are transformed according to that matrix during rendering.

The transformation applies only during rendering. The boundaries stored by the 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object are not altered by the <b>LinearGradientBrush::SetTransform</b> method.


#### Examples



The following example creates a linear gradient brush and uses it to fill a rectangle. Next, the code modifies the brush's transformation matrix and fills a rectangle with the transformed brush.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTransform(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush( 
      Rect(0, 0, 100, 50),
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 0, 255),  // blue
      LinearGradientModeHorizontal);

   Matrix matrix(2.0, 0, 0, 1, 0, 0);  // horizontal doubling

   // Fill a large area with the linear gradient brush (no transformation).
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 800, 50);

   linGrBrush.SetTransform(&amp;matrix);

   // Fill a large area with the transformed linear gradient brush.
   myGraphics.FillRectangle(&amp;linGrBrush, 0, 75, 800, 50);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/9b0236b2-be6b-4918-a106-5b0e6c3dd5ff">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/b6c00411-5017-4b0d-83fc-a9a3b2917511">LinearGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/2adb37e4-230c-4b65-ba7e-6b2dd7815f3e">LinearGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

