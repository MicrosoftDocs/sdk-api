---
UID: NF:gdiplusgraphics.Graphics.BeginContainer~r3
title: Graphics::BeginContainer
description: The Graphics::BeginContainer~r3 method (gdiplusgraphics.h) begins a new graphics container.
ms.date: 08/19/2022
ms.keywords: Graphics::BeginContainer
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Graphics::BeginContainer
 - gdiplusgraphics/Graphics::BeginContainer
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusgraphics.h
api_name:
 - Graphics::BeginContainer
---

# Graphics::BeginContainer


## -description

The <b>Graphics::BeginContainer</b> method begins a new graphics container.



## -returns

Type: <b>GraphicsContainer</b>

This method returns a value that identifies the container.

## -remarks

Use this method to create nested graphics containers. Graphics containers are used to retain graphics state, such as transformations, clipping regions, and various rendering properties.

The <b>Graphics::BeginContainer</b> method returns a value of type 
				<a href="/windows/desktop/gdiplus/-gdiplus-graphics-containers-about">GraphicsContainer</a>. When you have finished using a container, pass that value to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a> method. The 
				GraphicsContainer data type is defined in Gdiplusenums.h.

When you call the <b>Graphics::BeginContainer</b> method of a 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object, an information block that holds the state of the 
				<b>Graphics</b> object is put on a stack. The <b>Graphics::BeginContainer</b> method returns a value that identifies that information block. When you pass the identifying value to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a> method, the information block is removed from the stack and is used to restore the 
				<b>Graphics</b> object to the state it was in at the time of the <b>Graphics::BeginContainer</b> call.

Containers can be nested; that is, you can call the <b>Graphics::BeginContainer</b> method several times before you call the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a> method. Each time you call the <b>Graphics::BeginContainer</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::EndContainer</b> method, the 
				<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object is returned to the state it was in at the time of the <b>Graphics::BeginContainer</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::BeginContainer</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::BeginContainer</b> call are also removed.

Calls to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-save">Graphics::Save</a> method place information blocks on the same stack as calls to the <b>Graphics::BeginContainer</b> method. Just as an <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a> call is paired with a <b>Graphics::BeginContainer</b> call, a <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a> call is paired with a <b>Graphics::Save</b> call.

<div class="alert"><b>Caution</b>  When you call <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a>, all information blocks placed on the stack (by <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-save">Graphics::Save</a> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::BeginContainer</b> are removed from the stack. Likewise, when you call <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack.</div>
<div> </div>
For more information about graphics containers, see <a href="/windows/desktop/gdiplus/-gdiplus-nested-graphics-containers-use">Nested Graphics Containers</a>.


#### Examples

The following example sets a clipping region for a 
						<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object and begins a graphics container. It then sets an additional clipping region for the container and draws rectangles that demonstrate the effective clipping region inside the container.


```cpp
VOID Example_BeginContainer(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the clipping region for the Graphics object.
   graphics.SetClip(Rect(10, 10, 150, 150));

   // Begin a graphics container.
   GraphicsContainer container = graphics.BeginContainer();

   // Set an additional clipping region for the container.
   graphics.SetClip(Rect(100, 50, 100, 75));

   // Fill a red rectangle in the container.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillRectangle(&redBrush, 0, 0, 400, 400);

   // End the container, and fill the same rectangle with blue. 
   graphics.EndContainer(container);
   SolidBrush blueBrush(Color(128, 0, 0, 255));
   graphics.FillRectangle(&blueBrush, 0, 0, 400, 400);

   // Set the clipping region to infinite, and draw the outlines 
   // of the two previous clipping regions.
   graphics.ResetClip();
   Pen blackPen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&blackPen, 10, 10, 150, 150);
   graphics.DrawRectangle(&blackPen, 100, 50, 100, 75);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-graphics-containers-about">Graphics Containers</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-save">Graphics::Save</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-graphics-containers-use">Using Graphics Containers</a>
