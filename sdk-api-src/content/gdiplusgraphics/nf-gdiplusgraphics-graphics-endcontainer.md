---
UID: NF:gdiplusgraphics.Graphics.EndContainer
title: Graphics::EndContainer
author: windows-sdk-content
description: The Graphics::EndContainer method closes a graphics container that was previously opened by the Graphics::BeginContainer method.
old-location: gdiplus\_gdiplus_CLASS_Graphics_EndContainer_state_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\endcontainer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EndContainer, EndContainer method [GDI+], EndContainer method [GDI+],Graphics class, Graphics class [GDI+],EndContainer method, Graphics.EndContainer, Graphics::EndContainer, _gdiplus_CLASS_Graphics_EndContainer_state_, gdiplus._gdiplus_CLASS_Graphics_EndContainer_state_
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
 - Graphics.EndContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::EndContainer


## -description


The <b>Graphics::EndContainer</b> method closes a graphics container that was previously opened by the <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a> method.


## -parameters




### -param state [in]

Type: <b>GraphicsContainer</b>

Value (previously returned by <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a>) that identifies the container to be closed. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



When you call the <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a> method of a 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object, an information block that holds the state of the 
				<b>Graphics</b>object is put on a stack. The <b>Graphics::BeginContainer</b> method returns a value that identifies that information block. When you pass the identifying value to the <b>Graphics::EndContainer</b> method, the information block is removed from the stack and is used to restore the 
				<b>Graphics</b>object to the state it was in at the time of the <b>Graphics::BeginContainer</b> call.

Containers can be nested; that is, you can call the <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a> method several times before you call the <b>Graphics::EndContainer</b> method. Each time you call the <b>Graphics::BeginContainer</b> method, an information block is put on the stack, and you receive an identifier for the information block. When you pass one of those identifiers to the <b>Graphics::EndContainer</b> method, the 
				<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object is returned to the state it was in at the time of the <b>Graphics::BeginContainer</b> call that returned that particular identifier. The information block placed on the stack by that <b>Graphics::BeginContainer</b> call is removed from the stack, and all information blocks placed on that stack after that <b>Graphics::BeginContainer</b> call are also removed.

Calls to the <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> method place information blocks on the same stack as calls to the <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a> method. Just as an <b>Graphics::EndContainer</b> call is paired with a <b>Graphics::BeginContainer</b> call, a <a href="https://msdn.microsoft.com/34058862-9b3f-4ad4-bf57-904bbea50c4d">Graphics::Restore</a> call is paired with a <b>Graphics::Save</b> call.

<div class="alert"><b>Caution</b>  When you call <b>Graphics::EndContainer</b>, all information blocks placed on the stack (by <a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a> or by <a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a>) after the corresponding call to <b>Graphics::BeginContainer</b> are removed from the stack. Likewise, when you call <a href="https://msdn.microsoft.com/34058862-9b3f-4ad4-bf57-904bbea50c4d">Graphics::Restore</a>, all information blocks placed on the stack (by <b>Graphics::Save</b> or by <b>Graphics::BeginContainer</b>) after the corresponding call to <b>Graphics::Save</b> are removed from the stack.</div>
<div> </div>

#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>object and sets its clipping region. The code begins a container and sets an additional clipping region for the container. The code fills a rectangle twice: once inside the container, and once outside the container (after the call to <b>Graphics::EndContainer</b>).


```cpp
VOID Example_EndContainer(HDC hdc)
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
   graphics.FillRectangle(&redBrush, 0, 0, 200, 200);

   // End the container, and fill the same rectangle with blue. 
   graphics.EndContainer(container);
   SolidBrush blueBrush(Color(128, 0, 0, 255));
   graphics.FillRectangle(&blueBrush, 0, 0, 200, 200);

   // Set the clipping region to infinite, and draw 
   // the two previous clipping regions.
   graphics.ResetClip();
   Pen blackPen(Color(255, 0, 0, 0), 2.0f);
   graphics.DrawRectangle(&blackPen, 10, 10, 150, 150);
   graphics.DrawRectangle(&blackPen, 100, 50, 100, 75);
}
```





## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/98b9fa12-02e7-42bf-9cbd-03ee696188f6">Graphics Containers</a>



<a href="https://msdn.microsoft.com/90d2c126-01ed-4ff3-af99-a79a88c48ce5">Graphics::BeginContainer</a>



<a href="https://msdn.microsoft.com/34058862-9b3f-4ad4-bf57-904bbea50c4d">Graphics::Restore</a>



<a href="https://msdn.microsoft.com/fb281046-e995-44a4-a45f-72a85f1d5c5f">Graphics::Save</a>



<a href="https://msdn.microsoft.com/721d0c1c-d105-4d9f-b5e9-6ca407b28c4e">Using Graphics Containers</a>
 

 

