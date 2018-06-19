---
UID: NF:msinkaut.IInkOverlay.get_Renderer
title: IInkOverlay::get_Renderer
author: windows-sdk-content
description: Gets or sets the InkRenderer object that is used to draw ink.
old-location: tablet\inkoverlay_renderer.htm
old-project: tablet
ms.assetid: 1f43fa5a-1b08-41bc-9871-f4e0c53b61e9
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IInkOverlay interface [Tablet PC],Renderer property, IInkOverlay.Renderer, IInkOverlay.get_Renderer, IInkOverlay::Renderer, IInkOverlay::get_Renderer, IInkOverlay::put_Renderer, InkOverlay.get_Renderer, InkOverlay.put_Renderer, Renderer property [Tablet PC], Renderer property [Tablet PC],IInkOverlay interface, get_Renderer, msinkaut/IInkOverlay::Renderer, msinkaut/IInkOverlay::get_Renderer, msinkaut/IInkOverlay::put_Renderer, putref_Renderer, tablet.inkoverlay_renderer
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.Renderer
 - IInkOverlay.get_Renderer
 - IInkOverlay.put_Renderer
 - InkOverlay.get_Renderer
 - InkOverlay.put_Renderer
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::get_Renderer


## -description



Gets or sets the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object that is used to draw ink.



This property is read/write.


## -parameters


## -remarks



When handling certain window messages, changing the <b>Renderer</b> associated with the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> can cause a reentrant function call, generating unexpected results. For example, changing to a different <i>Renderer</i> or modifying its transforms within a message handler can result in a reentrant call. This affects the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). It is an issue with single-threaded apartment model applications.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms698599(v=vs.85).aspx">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>
 

 

