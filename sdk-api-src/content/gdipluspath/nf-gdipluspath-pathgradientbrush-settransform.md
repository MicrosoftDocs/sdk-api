---
UID: NF:gdipluspath.PathGradientBrush.SetTransform
title: PathGradientBrush::SetTransform
author: windows-sdk-content
description: The PathGradientBrush::SetTransform method sets the transformation matrix of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\settransform_69matrix.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: PathGradientBrush class [GDI+],SetTransform method, PathGradientBrush.SetTransform, PathGradientBrush::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetTransform_matrix_
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
 - PathGradientBrush.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetTransform


## -description


The <b>PathGradientBrush::SetTransform</b> method sets the transformation matrix of this path gradient brush.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a 
					<b>Matrix</b> object that specifies the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object has a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object that serves as the boundary path for the brush. When you paint with a path gradient brush, only the area inside the boundary path is filled. If the brush's transformation matrix is set to represent any transformation other than the identity, then the boundary path is transformed according to that matrix during rendering, and only the area inside the transformed path is filled.

The transformation applies only during rendering. The boundary path stored by the 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object is not altered by the <b>PathGradientBrush::SetTransform</b> method.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>object based on a triangular path. The 
						<a href="https://msdn.microsoft.com/91d3fc66-4c0d-4b44-beae-59f13b80483d">Graphics::FillRectangle</a> method uses the path gradient brush to paint a rectangle that contains the triangular path. Next, the code creates a 
						<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that represents a composite transformation (rotate, then translate) and passes the address of that 
						<b>Matrix</b> object to the <b>PathGradientBrush::SetTransform</b> method of the 
						<b>PathGradientBrush</b>object. The code calls 
						<a href="https://msdn.microsoft.com/eff3454e-f4d7-4cc2-9385-268d9ced2715">FillRectangle</a> a second time to paint the same rectangle using the transformed path gradient brush.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Point pts[] = {
      Point(0, 0), 
      Point(100, 0), 
      Point(100, 100)};

   Color cols[] = {
      Color(255, 255, 0, 0),  // red
      Color(255, 0, 255, 0),  // green
      Color(255, 0, 0, 0)};   // black

   INT count = 3;
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.SetSurroundColors(cols, &amp;count);

   // Fill an area with the path gradient brush (no transformation).
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 200, 200);

   // Set the transformation for the brush (rotate, then translate).
   Matrix matrix(0.0f, 1.0f, -1.0f, 0.0f, 150.0f, 60.0f);
   pthGrBrush.SetTransform(&amp;matrix);
   
   // Fill the same area with the transformed path gradient brush.
   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 200, 200);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/f74e7b87-4b8b-4f2e-81a5-d8905b5e6351">PathGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/96bb8813-1dbf-48ae-adf8-a9a0f3bc210f">PathGradientBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/41b3160d-ce08-413e-b2f6-3d7ad11dbde5">PathGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/00f7172b-2967-4d17-b6a6-daeec6d3eb33">PathGradientBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/3e6d8b19-92a7-4e3c-983d-8f13e4a8f4ee">PathGradientBrush::TranslateTransform</a>
 

 

