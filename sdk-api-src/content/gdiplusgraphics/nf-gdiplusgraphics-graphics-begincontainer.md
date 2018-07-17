---
UID: NF:gdiplusgraphics.Graphics.BeginContainer
title: Graphics::BeginContainer
author: windows-sdk-content
description: The Graphics::BeginContainer method begins a new graphics container.
old-location: gdiplus\_gdiplus_CLASS_Graphics_BeginContainer_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsbegincontainermethods\begincontainer.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: BeginContainer, BeginContainer method [GDI+], BeginContainer method [GDI+],Graphics class, Graphics class [GDI+],BeginContainer method, Graphics.BeginContainer, Graphics.BeginContainer(), Graphics::BeginContainer, _gdiplus_CLASS_Graphics_BeginContainer_, gdiplus._gdiplus_CLASS_Graphics_BeginContainer_
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
 - Graphics.BeginContainer
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::BeginContainer


## -description


The <b>Graphics::BeginContainer</b> method begins a new graphics container. 


## -parameters




### -param dstrect




### -param srcrect




### -param unit






## -returns



Type: <strong>Type: <b>GraphicsContainer</b>
</strong>

This method returns a value that identifies the container.




## -remarks



Use this method to create nested graphics containers. Graphics containers are used to retain graphics state, such as transformations, clipping regions, and various rendering properties.

The <b>Graphics::BeginContainer</b> method returns a value of type 
				<a href="https://msdn.microsoft.com/library/ms536334(v=VS.85).aspx">GraphicsContainer</a>. When you have finished using a container, pass that value to the <a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method. The 
				GraphicsContainer data type is defined in Gdiplusenums.h.

When you call the <b>Graphics::BeginContainer</b> method of a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, an information block that holds the state of the 
				<b>Graphics</b> object is put on a stack. The <b>Graphics::BeginContainer</b> method returns a value that identifies that information block. When you pass the identifying value to the <a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method, the information block is removed from the stack and is used to restore the 
				<b>Graphics</b> object to the state it was in at the time of the <b>Graphics::BeginContainer</b> call.

Containers can be nested; that is, you can call the <b>Graphics::BeginContainer</b> method several times before you call the <a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> method. Each time you call the <b>Graphics::BeginContainer</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::EndContainer</b> method, the 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is returned to the state it was in at the time of the <b>Graphics::BeginContainer</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::BeginContainer</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::BeginContainer</b> call are also removed.

Calls to the <a href="https://msdn.microsoft.com/library/ms535806(v=VS.85).aspx">Graphics::Save</a> method place information blocks on the same stack as calls to the <b>Graphics::BeginContainer</b> method. Just as an <a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a> call is paired with a <b>Graphics::BeginContainer</b> call, a <a href="https://msdn.microsoft.com/library/ms535804(v=VS.85).aspx">Graphics::Restore</a> call is paired with a <b>Graphics::Save</b> call.

<div class="alert"><b>Caution</b>  When you call <a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a>, all information blocks placed on the stack (by <a href="https://msdn.microsoft.com/library/ms535806(v=VS.85).aspx">Graphics::Save</a> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::BeginContainer</b> are removed from the stack. Likewise, when you call <a href="https://msdn.microsoft.com/library/ms535804(v=VS.85).aspx">Graphics::Restore</a>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack.</div>
<div> </div>
For more information about graphics containers, see <a href="https://msdn.microsoft.com/library/ms533848(v=VS.85).aspx">Nested Graphics Containers</a>.


#### Examples

The following example sets a clipping region for a 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object and begins a graphics container. It then sets an additional clipping region for the container and draws rectangles that demonstrate the effective clipping region inside the container.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_BeginContainer(HDC hdc)
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
   graphics.FillRectangle(&amp;redBrush, 0, 0, 400, 400);

   // End the container, and fill the same rectangle with blue. 
   graphics.EndContainer(container);
   SolidBrush blueBrush(Color(128, 0, 0, 255));
   graphics.FillRectangle(&amp;blueBrush, 0, 0, 400, 400);

   // Set the clipping region to infinite, and draw the outlines 
   // of the two previous clipping regions.
   graphics.ResetClip();
   Pen blackPen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&amp;blackPen, 10, 10, 150, 150);
   graphics.DrawRectangle(&amp;blackPen, 100, 50, 100, 75);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/library/ms536334(v=VS.85).aspx">Graphics Containers</a>



<a href="https://msdn.microsoft.com/library/ms535686(v=VS.85).aspx">Graphics::EndContainer</a>



<a href="https://msdn.microsoft.com/library/ms535804(v=VS.85).aspx">Graphics::Restore</a>



<a href="https://msdn.microsoft.com/library/ms535806(v=VS.85).aspx">Graphics::Save</a>



<a href="https://msdn.microsoft.com/library/ms533813(v=VS.85).aspx">Using Graphics Containers</a>
 

 

