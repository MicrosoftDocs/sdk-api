---
UID: NF:msinkaut.IInkCursor.get_Inverted
title: IInkCursor::get_Inverted
author: windows-sdk-content
description: Gets a value that indicates whether the cursor is the inverted end of the pen.
old-location: tablet\iinkcursor_inverted.htm
tech.root: tablet
ms.assetid: 83cc33ba-0887-4f04-8eaf-325fcf90b8fe
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 83cc33ba-0887-4f04-8eaf-325fcf90b8fe, IInkCursor interface [Tablet PC],Inverted property, IInkCursor.Inverted, IInkCursor.get_Inverted, IInkCursor::Inverted, IInkCursor::get_Inverted, Inverted property [Tablet PC], Inverted property [Tablet PC],IInkCursor interface, get_Inverted, msinkaut/IInkCursor::Inverted, msinkaut/IInkCursor::get_Inverted, tablet.iinkcursor_inverted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCursor.Inverted
 - IInkCursor.get_Inverted
 - IInkCursor.get_Inverted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCursor::get_Inverted


## -description



Gets a value that indicates whether the cursor is the inverted end of the pen.



This property is read-only.


## -parameters


## -remarks



Inverted cursors are generally associated with erasing. A pen might have one end that is intended for drawing and another intended for erasing. For more information about erasing ink, see <a href="https://msdn.microsoft.com/9851c871-4d1c-43b6-9615-5d231cbc01ae">Erasing Ink with the Pen</a>.

Whether or not you use the <b>Inverted</b> property is entirely up to the needs of your application. Applications are not required to inspect inverted cursors, and the <i>ink collector</i> applies default drawing attributes to inverted cursors just as it does to cursors that are not inverted.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to <b>SC_HOTKEY</b> or <b>SC_TASKLIST</b>; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">InkCursor Interface</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>
 

 

