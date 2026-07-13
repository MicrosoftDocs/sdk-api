---
UID: NF:gdiplusgraphics.Graphics.Save
title: Graphics::Save (gdiplusgraphics.h)
description: The Graphics::Save method saves the current state (transformations, clipping region, and quality settings) of this Graphics object. You can restore the state later by calling the Graphics::Restore method.
helpviewer_keywords: ["Graphics class [GDI+]","Save method","Graphics.Save","Graphics::Save","Save","Save method [GDI+]","Save method [GDI+]","Graphics class","_gdiplus_CLASS_Graphics_Save_","gdiplus._gdiplus_CLASS_Graphics_Save_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Save_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\save.htm
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],Save method, Graphics.Save, Graphics::Save, Save, Save method [GDI+], Save method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_Save_, gdiplus._gdiplus_CLASS_Graphics_Save_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::Save
 - gdiplusgraphics/Graphics::Save
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
 - Graphics.Save
---

# Graphics::Save


## -description

The <b>Graphics::Save</b> method saves the current state (transformations, clipping region, and quality settings) of this <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. You can restore the state later by calling the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method.



## -returns

Type: <b>GraphicsState</b>

This method returns a value that identifies the saved state. Pass this value to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method when you want to restore the state. The <b>GraphicsState</b> data type is defined in Gdiplusenums.h.

## -remarks

When you call the <b>Graphics::Save</b> method of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, an information block that holds the state of the <b>Graphics</b> object is put on a stack. The <b>Graphics::Save</b> method returns a value that identifies that information block. When you pass the identifying value to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method, the information block is removed from the stack and is used to restore the <b>Graphics</b> object to the state it was in at the time of the <b>Graphics::Save</b> call. Note that the identifier returned by a given call to the <b>Graphics::Save</b> method can be passed only once to the <b>Graphics::Restore</b> method.

Calls to the <b>Graphics::Save</b> method can be nested; that is, you can call the <b>Graphics::Save</b> method several times before you call the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method. Each time you call the <b>Graphics::Save</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::Restore</b> method, the <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is returned to the state it was in at the time of the <b>Graphics::Save</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::Save</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::Save</b> call are also removed.

Calls to the <b>BeginContainer</b> method place information blocks on the same stack as calls to the <b>Graphics::Save</b> method. Just as a <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> call is paired with a <b>Graphics::Save</b> call, an <b>EndContainer</b> call is paired with a <b>BeginContainer</b> call.

<div class="alert"><b>Note</b>  When you call <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack. Likewise, When you call <b>EndContainer</b>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>BeginContainer</b>) after the corresponding call to <b>BeginContainer</b> are removed from the stack.</div>
<div> </div>

#### Examples

The following examples show two ways to use the <b>Graphics::Save</b> method. The first example shows how to restore nested saved states, and the second example shows how to restore only the first of two nested saved states.

<b>Restoring Nested Saved States</b>

The following example sets the world transformation of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a rotation and then saves the state of the <b>Graphics</b> object. Next, the code calls <b>TranslateTransform</b>, and saves the state again. Then the code calls <b>ScaleTransform</b>. At that point, the world transformation of the <b>Graphics</b> object is a composite transformation: first rotate, then translate, then scale. The code uses a red pen to draw an ellipse that is transformed by that composite transformation.

The code passes <i>state2</i>, which was returned by the second call to <b>Save</b>, to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method, and draws the ellipse again using a green pen. The green ellipse is rotated and translated but not scaled. Finally the code passes state1, which was returned by the first call to <b>Save</b>, to the <b>Graphics::Restore</b> method, and draws the ellipse again using a blue pen. The blue ellipse is rotated but not translated or scaled.


```cpp
VOID Example_Save1(HDC hdc)
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
   graphics.DrawEllipse(&redPen, 0, 0, 100, 20);
 
   // Restore to state2 and draw the ellipse again. 
   // Two transformations apply: rotate then translate.
   graphics.Restore(state2);
   Pen greenPen(Color(255, 0, 255, 0));
   graphics.DrawEllipse(&greenPen, 0, 0, 100, 20);

   // Restore to state1 and draw the ellipse again. 
   // Only the rotation transformation applies.
   graphics.Restore(state1);
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawEllipse(&bluePen, 0, 0, 100, 20);
}

```


<b>Restoring Only the First of Two Nested Saved States</b>

The following example sets the world transformation of a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object to a rotation and then saves the state of the <b>Graphics</b> object. Next, the code calls <b>TranslateTransform</b>, and saves the state again. Then the code calls <b>ScaleTransform</b>. At that point, the world transformation of the <b>Graphics</b> object is a composite transformation: first rotate, then translate, then scale. The code uses a red pen to draw an ellipse that is transformed by that composite transformation.

The code passes <i>state1</i>, which was returned by the first call to <b>Save</b>, to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> method, and draws the ellipse again using a green pen. The green ellipse is rotated but not translated or scaled. 

Next the code attempts to restore the state identified by <i>state2</i>. The attempt fails because the call Restore(<i>state1</i>) removed the information blocks identified by both <i>state1</i> and <i>state2</i> from the stack.


```cpp
VOID Example_Save2(HDC hdc)
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
   graphics.DrawEllipse(&redPen, 0, 0, 100, 20);
 
   // Restore to state1 and draw the ellipse again. 
   // Only the rotation transformation applies.
   graphics.Restore(state1);
   Pen greenPen(Color(255, 0, 255, 0));
   graphics.DrawEllipse(&greenPen, 0, 0, 100, 20);

   // The information block identified by state2 has been lost.
   // The following call to Restore has no effect because
   // Restore(state1) removed from the stack the
   // information blocks identified by state1 and state2.
   graphics.Restore(state2);

   // The Graphics object is still in the state identified by state1.
   // The following code draws a blue ellipse on top of the previously
   // drawn green ellipse.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawEllipse(&bluePen, 0, 0, 100, 20);
}

```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a>
