---
UID: NF:msinkaut.IInkOverlay.put_MarginX
title: IInkOverlay::put_MarginX (msinkaut.h)
description: Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window. (IInkOverlay.put_MarginX)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","MarginX property","IInkOverlay.MarginX","IInkOverlay.put_MarginX","IInkOverlay::MarginX","IInkOverlay::get_MarginX","IInkOverlay::put_MarginX","InkOverlay.get_MarginX","InkOverlay.put_MarginX","MarginX property [Tablet PC]","MarginX property [Tablet PC]","IInkOverlay interface","get_MarginX","msinkaut/IInkOverlay::MarginX","msinkaut/IInkOverlay::get_MarginX","msinkaut/IInkOverlay::put_MarginX","put_MarginX","tablet.inkoverlay_marginx"]
old-location: tablet\inkoverlay_marginx.htm
tech.root: tablet
ms.assetid: 869fc2dc-ef9b-4427-a7e0-9a2b41b66fe8
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],MarginX property, IInkOverlay.MarginX, IInkOverlay.put_MarginX, IInkOverlay::MarginX, IInkOverlay::get_MarginX, IInkOverlay::put_MarginX, InkOverlay.get_MarginX, InkOverlay.put_MarginX, MarginX property [Tablet PC], MarginX property [Tablet PC],IInkOverlay interface, get_MarginX, msinkaut/IInkOverlay::MarginX, msinkaut/IInkOverlay::get_MarginX, msinkaut/IInkOverlay::put_MarginX, put_MarginX, tablet.inkoverlay_marginx
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
 - IInkOverlay::put_MarginX
 - msinkaut/IInkOverlay::put_MarginX
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
 - IInkOverlay.MarginX
 - IInkOverlay.get_MarginX
 - IInkOverlay.put_MarginX
 - InkOverlay.get_MarginX
 - InkOverlay.put_MarginX
---

# IInkOverlay::put_MarginX


## -description

Gets or sets the x-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.



This property is read/write.

## -parameters

## -remarks

This property is most commonly used with nonintegrated tablet devices?the buffer gives users a margin of error when writing on a device that may not map 1 to 1 with the screen.

The margin is specified in screen coordinates. A positive margin extends outside the context, a negative margin extends inside the context, and a value of zero produces no margin. Ink is collected if the stroke starts within the margin. This behavior does not clip the ink. The context of the object or control is either the window input rectangle from the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle">GetWindowInputRectangle</a> method or the client rectangle for the window.

The margin is effective only within the application's window. If the pen is applied outside the application's window, then the application loses focus and cannot collect ink.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> object, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. To disable inking in the <b>InkOverlay</b> control, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. You can then set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx">MarginX</a> property, and re-enable the object or control by setting the <b>Enabled</b> property (or <b>InkEnabled</b> property) to <b>TRUE</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled Property</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy">MarginY Property</a>
