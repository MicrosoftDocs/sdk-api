---
UID: NF:gdiplusbrush.LinearGradientBrush.SetTransform
title: LinearGradientBrush::SetTransform
author: windows-sdk-content
description: The LinearGradientBrush::SetTransform method sets the transformation matrix of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\settransform_65matrix.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: LinearGradientBrush class [GDI+],SetTransform method, LinearGradientBrush.SetTransform, LinearGradientBrush::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetTransform_matrix_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KnownGamingPrivileges
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::SetTransform


## -description


The <b>LinearGradientBrush::SetTransform</b> method sets the transformation matrix of this linear gradient brush.


## -parameters




### -param matrix [in]

Type: <b>const Matrix*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object has a rectangle that specifies the starting and ending boundaries of the gradient and a mode or angle that affects the direction. If the brush's transformation matrix is set to represent any transformation other than the identity, then the boundaries and direction are transformed according to that matrix during rendering.

The transformation applies only during rendering. The boundaries stored by the 
				<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object are not altered by the <b>LinearGradientBrush::SetTransform</b> method.


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




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533914(v=VS.85).aspx">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533806(v=VS.85).aspx">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535335(v=VS.85).aspx">LinearGradientBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535339(v=VS.85).aspx">LinearGradientBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

