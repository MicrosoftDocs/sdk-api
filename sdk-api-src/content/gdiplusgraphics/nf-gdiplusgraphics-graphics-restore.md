---
UID: NF:gdiplusgraphics.Graphics.Restore
title: Graphics::Restore
author: windows-sdk-content
description: The Graphics::Restore method sets the state of this Graphics object to the state stored by a previous call to the Graphics::Save method of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_Restore_gstate_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\restore.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Graphics class [GDI+],Restore method, Graphics.Restore, Graphics::Restore, Restore, Restore method [GDI+], Restore method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_Restore_gstate_, gdiplus._gdiplus_CLASS_Graphics_Restore_gstate_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.Restore
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::Restore


## -description


The <b>Graphics::Restore</b> method sets the state of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to the state stored by a previous call to the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method of this <b>Graphics</b> object.


## -parameters




### -param gstate [in]

Type: <b>GraphicsState</b>

32-bit value (returned by a previous call to the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object) that identifies a block of saved state. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



When you call the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, an information block that holds the state of the <b>Graphics</b> object is put on a stack. The <b>Graphics::Save</b> method returns a value that identifies that information block. When you pass the identifying value to the <b>Restore</b> method, the information block is removed from the stack and is used to restore the <b>Graphics</b> object to the state it was in at the time of the <b>Graphics::Save</b> call. Note that the identifier returned by a given call to the <b>Graphics::Save</b> method can be passed only once to the <b>Graphics::Restore</b> method.

Calls to the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method can be nested; that is, you can call the <b>Graphics::Save</b> method several times before you call the <b>Graphics::Restore</b> method. Each time you call the <b>Graphics::Save</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::Restore</b> method, the <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is returned to the state it was in at the time of the <b>Graphics::Save</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::Save</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::Save</b> call are also removed.

Calls to the <b>BeginContainer</b> method place information blocks on the same stack as calls to the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method. Just as a <b>Graphics::Restore</b> call is paired with a <b>Graphics::Save</b> call, an <b>EndContainer</b> call is paired with a <b>BeginContainer</b> call.

<div class="alert"><b>Note</b>  When you call <b>Graphics::Restore</b>, all information blocks placed on the stack (by <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> or by <b>BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack. Likewise, When you call <b>EndContainer</b>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>BeginContainer</b>) after the corresponding call to <b>BeginContainer</b> are removed from the stack.</div>
<div> </div>

#### Examples

The following examples show two ways to use the <b>Graphics::Restore</b> method. The first example shows how to restore nested saved states, and the second example shows how to restore only the first of two nested saved states.

<b>Restoring Nested Saved States</b>

The following example sets the world transformation of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a rotation and then saves the state of the <b>Graphics</b> object. Next, the code calls <b>TranslateTransform</b>, and saves the state again. Then the code calls <b>ScaleTransform</b>. At that point, the world transformation of the <b>Graphics</b> object is a composite transformation: first rotate, then translate, then scale. The code uses a red pen to draw an ellipse that is transformed by that composite transformation.

The code passes <i>state2</i>, which was returned by the second call to <b>Save</b>, to the <b>Graphics::Restore</b> method, and draws the ellipse again using a green pen. The green ellipse is rotated and translated but not scaled. Finally the code passes state1, which was returned by the first call to <b>Save</b>, to the <b>Graphics::Restore</b> method, and draws the ellipse again using a blue pen. The blue ellipse is rotated but not translated or scaled.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Save1(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsState state1, state2;

   graphics.RotateTransform(30.0f);
   state1 = graphics.Save();
   graphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
   state2 = graphics.Save();
   graphics.ScaleTransform(1.0f, 3.0f, MatrixOrderAppend);
   
   // Draw an ellipse. 
   // Three transformations apply: rotate, then translate, then scale.
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawEllipse(&amp;redPen, 0, 0, 100, 20);
 
   // Restore to state2 and draw the ellipse again. 
   // Two transformations apply: rotate then translate.
   graphics.Restore(state2);
   Pen greenPen(Color(255, 0, 255, 0));
   graphics.DrawEllipse(&amp;greenPen, 0, 0, 100, 20);

   // Restore to state1 and draw the ellipse again. 
   // Only the rotation transformation applies.
   graphics.Restore(state1);
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawEllipse(&amp;bluePen, 0, 0, 100, 20);
}
</pre>
</td>
</tr>
</table></span></div>
<b>Restoring Only the First of Two Nested Saved States</b>

The following example sets the world transformation of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a rotation and then saves the state of the <b>Graphics</b> object. Next, the code calls <b>TranslateTransform</b>, and saves the state again. Then the code calls <b>ScaleTransform</b>. At that point, the world transformation of the <b>Graphics</b> object is a composite transformation: first rotate, then translate, then scale. The code uses a red pen to draw an ellipse that is transformed by that composite transformation.

The code passes <i>state1</i>, which was returned by the first call to <b>Save</b>, to the <b>Graphics::Restore</b> method, and draws the ellipse again using a green pen. The green ellipse is rotated but not translated or scaled. 

Next the code attempts to restore the state identified by <i>state2</i>. The attempt fails because the call Restore(<i>state1</i>) removed the information blocks identified by both <i>state1</i> and <i>state2</i> from the stack.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Save2(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsState state1, state2;

   graphics.RotateTransform(30.0f);
   state1 = graphics.Save();
   graphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
   state2 = graphics.Save();
   graphics.ScaleTransform(1.0f, 3.0f, MatrixOrderAppend);
   
   // Draw an ellipse. 
   // Three transformations apply: rotate, then translate, then scale.
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawEllipse(&amp;redPen, 0, 0, 100, 20);
 
   // Restore to state1 and draw the ellipse again. 
   // Only the rotation transformation applies.
   graphics.Restore(state1);
   Pen greenPen(Color(255, 0, 255, 0));
   graphics.DrawEllipse(&amp;greenPen, 0, 0, 100, 20);

   // The information block identified by state2 has been lost.
   // The following call to Restore has no effect because
   // Restore(state1) removed from the stack the
   // information blocks identified by state1 and state2.
   graphics.Restore(state2);

   // The Graphics object is still in the state identified by state1.
   // The following code draws a blue ellipse on top of the previously
   // drawn green ellipse.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawEllipse(&amp;bluePen, 0, 0, 100, 20);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a>
 

 

