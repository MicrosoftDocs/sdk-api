---
UID: NF:gdiplusgraphics.Graphics.BeginContainer(constRect&,constRect&,Unit)
title: Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit) (gdiplusgraphics.h)
description: The Graphics::BeginContainer method begins a new graphics container. (overload 1/2)
helpviewer_keywords: ["BeginContainer","BeginContainer method [GDI+]","BeginContainer method [GDI+]","Graphics class","Graphics class [GDI+]","BeginContainer method","Graphics.BeginContainer","Graphics.BeginContainer(IN const Rect &","IN const Rect &","IN Unit)","Graphics.BeginContainer(const Rect&","const Rect&","Unit)","Graphics::BeginContainer","Graphics::BeginContainer(IN const Rect &","IN const Rect &","IN Unit)","_gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_","gdiplus._gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsbegincontainermethods\begincontainer_69rectampdstrect_rectampsrcrect_unitunit.htm
ms.date: 12/05/2018
ms.keywords: BeginContainer, BeginContainer method [GDI+], BeginContainer method [GDI+],Graphics class, Graphics class [GDI+],BeginContainer method, Graphics.BeginContainer, Graphics.BeginContainer(IN const Rect &,IN const Rect &,IN Unit), Graphics.BeginContainer(const Rect&,const Rect&,Unit), Graphics::BeginContainer, Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit), _gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_, gdiplus._gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_
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
 - Graphics::BeginContainer
 - gdiplusgraphics/Graphics::BeginContainer
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
 - Graphics.BeginContainer
---

# Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit)


## -description

The <b>Graphics::BeginContainer</b> method begins a new graphics container.

## -parameters

### -param dstrect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that, together with <i>srcrect</i>, specifies a transformation for the container.

### -param srcrect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a></b>

Reference to a rectangle that, together with <i>dstrect</i>, specifies a transformation for the container.

### -param unit [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">Unit</a></b>

Unit of measure for the container.

## -returns

Type: <b>GraphicsContainer</b>

This method returns a value that identifies the container.

## -remarks

Use this method to create nested graphics containers. Graphics containers are used to retain graphics state, such as transformations, clipping regions, and various rendering properties.

The <b>Graphics::BeginContainer</b> method returns a value of type 
				<a href="/windows/desktop/gdiplus/-gdiplus-graphics-containers-about">GraphicsContainer</a>. When you have finished using a container, pass that value to the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a> method. The 
				GraphicsContainer data type is defined in Gdiplusenums.h.

The 
				<i>dstrect</i> and 
				<i>srcrect</i> parameters specify a transformation. It is the transformation that, when applied to 
				<i>srcrect</i>, results in 
				<i>dstrect</i>.

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

The following example calls the <b>Graphics::BeginContainer</b> method to create a graphics container. The code specifies a transformation for the container by passing two rectangles to the <b>Graphics::BeginContainer</b> method. The code calls 
						<a href="/previous-versions/ms535966(v=vs.85)">Graphics::FillEllipse</a> twice: once inside the container and once outside the container (after the call to <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a>).


```cpp
VOID Example_BeginContainer2(HDC hdc)
{
   Graphics graphics(hdc);

   // Define a translation and scale transformation for the container.
   Rect srcRect(0, 0, 200, 100);
   Rect destRect(100, 100, 200, 200);

   // Create a graphics container with a (100, 100) translation 
   // and (1, 2) scale.
   GraphicsContainer container;
   container = graphics.BeginContainer(destRect, srcRect, UnitPixel);

   // Fill an ellipse in the container.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   graphics.FillEllipse(&redBrush, 0, 0, 100, 60);

   // End the container.
   graphics.EndContainer(container);

   // Fill the same ellipse outside the container.
   SolidBrush blueBrush(Color(255, 0, 0, 255));
   graphics.FillEllipse(&blueBrush, 0, 0, 100, 60);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/gdiplus/-gdiplus-graphics-containers-about">Graphics Containers</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer">Graphics::EndContainer</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-restore">Graphics::Restore</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-save">Graphics::Save</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-graphics-containers-use">Using Graphics Containers</a>
