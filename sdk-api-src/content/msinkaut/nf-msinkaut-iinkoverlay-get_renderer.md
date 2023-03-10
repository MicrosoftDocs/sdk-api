---
UID: NF:msinkaut.IInkOverlay.get_Renderer
title: IInkOverlay::get_Renderer (msinkaut.h)
description: Gets or sets the InkRenderer object that is used to draw ink. (IInkOverlay.get_Renderer)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","Renderer property","IInkOverlay.Renderer","IInkOverlay.get_Renderer","IInkOverlay::Renderer","IInkOverlay::get_Renderer","IInkOverlay::put_Renderer","InkOverlay.get_Renderer","InkOverlay.put_Renderer","Renderer property [Tablet PC]","Renderer property [Tablet PC]","IInkOverlay interface","get_Renderer","msinkaut/IInkOverlay::Renderer","msinkaut/IInkOverlay::get_Renderer","msinkaut/IInkOverlay::put_Renderer","putref_Renderer","tablet.inkoverlay_renderer"]
old-location: tablet\inkoverlay_renderer.htm
tech.root: tablet
ms.assetid: 1f43fa5a-1b08-41bc-9871-f4e0c53b61e9
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],Renderer property, IInkOverlay.Renderer, IInkOverlay.get_Renderer, IInkOverlay::Renderer, IInkOverlay::get_Renderer, IInkOverlay::put_Renderer, InkOverlay.get_Renderer, InkOverlay.put_Renderer, Renderer property [Tablet PC], Renderer property [Tablet PC],IInkOverlay interface, get_Renderer, msinkaut/IInkOverlay::Renderer, msinkaut/IInkOverlay::get_Renderer, msinkaut/IInkOverlay::put_Renderer, putref_Renderer, tablet.inkoverlay_renderer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay::get_Renderer
 - msinkaut/IInkOverlay::get_Renderer
dev_langs:
 - c++
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
---

# IInkOverlay::get_Renderer


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkrenderer-class">InkRenderer</a> object that is used to draw ink.



This property is read/write.

## -parameters

## -remarks

When handling certain window messages, changing the <b>Renderer</b> associated with the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> can cause a reentrant function call, generating unexpected results. For example, changing to a different <i>Renderer</i> or modifying its transforms within a message handler can result in a reentrant call. This affects the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). It is an issue with single-threaded apartment model applications.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
