---
UID: NF:gdiplusgraphics.Graphics.BeginContainer(IN const Rect &,IN const Rect &,IN Unit)
title: Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit)
author: windows-sdk-content
description: The Graphics::BeginContainer method begins a new graphics container.
old-location: gdiplus\_gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsbegincontainermethods\begincontainer_69rectampdstrect_rectampsrcrect_unitunit.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: BeginContainer, BeginContainer method [GDI+], BeginContainer method [GDI+],Graphics class, Graphics class [GDI+],BeginContainer method, Graphics.BeginContainer, Graphics.BeginContainer(IN const Rect &,IN const Rect &,IN Unit), Graphics.BeginContainer(const Rect&,const Rect&,Unit), Graphics::BeginContainer, Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit), _gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_, gdiplus._gdiplus_CLASS_Graphics_BeginContainer_Rect_dstrect_Rect_srcrect_Unit_unit_
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
 - Graphics.BeginContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::BeginContainer(IN const Rect &,IN const Rect &,IN Unit)


## -description


The <b>Graphics::BeginContainer</b> method begins a new graphics container.


## -parameters




### -param dstrect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle that, together with 
					<i>srcrect</i>, specifies a transformation for the container. 


### -param srcrect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle that, together with 
					<i>dstrect</i>, specifies a transformation for the container. 


### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/33f0b0fd-7764-48bc-874e-26cc522d5362">Unit</a></b>

Unit of measure for the container. 


## -returns



Type: <strong>Type: <b>GraphicsContainer</b>
</strong>

This method returns a value that identifies the container.




## -remarks



Use this method to create nested graphics containers. Graphics containers are used to retain graphics state, such as transformations, clipping regions, and various rendering properties.

The <b>Graphics::BeginContainer</b> method returns a value of type 
				<a href="https://msdn.microsoft.com/en-us/library/ms536334(v=VS.85).aspx">GraphicsContainer</a>. When you have finished using a container, pass that value to the <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method. The 
				GraphicsContainer data type is defined in Gdiplusenums.h.

The 
				<i>dstrect</i> and 
				<i>srcrect</i> parameters specify a transformation. It is the transformation that, when applied to 
				<i>srcrect</i>, results in 
				<i>dstrect</i>.

When you call the <b>Graphics::BeginContainer</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object, an information block that holds the state of the 
				<b>Graphics</b> object is put on a stack. The <b>Graphics::BeginContainer</b> method returns a value that identifies that information block. When you pass the identifying value to the <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method, the information block is removed from the stack and is used to restore the 
				<b>Graphics</b> object to the state it was in at the time of the <b>Graphics::BeginContainer</b> call.

Containers can be nested; that is, you can call the <b>Graphics::BeginContainer</b> method several times before you call the <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method. Each time you call the <b>Graphics::BeginContainer</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::EndContainer</b> method, the 
				<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object is returned to the state it was in at the time of the <b>Graphics::BeginContainer</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::BeginContainer</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::BeginContainer</b> call are also removed.

Calls to the <a href="https://msdn.microsoft.com/en-us/library/ms535806(v=VS.85).aspx">Graphics::Save</a> method place information blocks on the same stack as calls to the <b>Graphics::BeginContainer</b> method. Just as an <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> call is paired with a <b>Graphics::BeginContainer</b> call, a <a href="https://msdn.microsoft.com/en-us/library/ms535804(v=VS.85).aspx">Graphics::Restore</a> call is paired with a <b>Graphics::Save</b> call.

<div class="alert"><b>Caution</b>  When you call <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a>, all information blocks placed on the stack (by <a href="https://msdn.microsoft.com/en-us/library/ms535806(v=VS.85).aspx">Graphics::Save</a> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::BeginContainer</b> are removed from the stack. Likewise, when you call <a href="https://msdn.microsoft.com/en-us/library/ms535804(v=VS.85).aspx">Graphics::Restore</a>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack.</div>
<div> </div>
For more information about graphics containers, see <a href="https://msdn.microsoft.com/en-us/library/ms533848(v=VS.85).aspx">Nested Graphics Containers</a>.


#### Examples

The following example calls the <b>Graphics::BeginContainer</b> method to create a graphics container. The code specifies a transformation for the container by passing two rectangles to the <b>Graphics::BeginContainer</b> method. The code calls 
						<a href="https://msdn.microsoft.com/77f8e3d0-56f4-4fd5-b18c-b4734e98a987">Graphics::FillEllipse</a> twice: once inside the container and once outside the container (after the call to <a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a>).


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




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536334(v=VS.85).aspx">Graphics Containers</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535804(v=VS.85).aspx">Graphics::Restore</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535806(v=VS.85).aspx">Graphics::Save</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533813(v=VS.85).aspx">Using Graphics Containers</a>
 

 

