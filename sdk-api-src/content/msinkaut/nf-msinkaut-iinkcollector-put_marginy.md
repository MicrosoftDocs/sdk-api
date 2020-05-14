---
UID: NF:msinkaut.IInkCollector.put_MarginY
title: IInkCollector::put_MarginY (msinkaut.h)
description: Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window.helpviewer_keywords: ["6cba076e-6392-4f0a-a80d-3df903d0ba13","IInkCollector interface [Tablet PC]","MarginY property","IInkCollector.MarginY","IInkCollector.put_MarginY","IInkCollector::MarginY","IInkCollector::get_MarginY","IInkCollector::put_MarginY","InkCollector.get_MarginY","InkCollector.put_MarginY","MarginY property [Tablet PC]","MarginY property [Tablet PC]","IInkCollector interface","msinkaut/IInkCollector::MarginY","msinkaut/IInkCollector::get_MarginY","msinkaut/IInkCollector::put_MarginY","put_MarginY","tablet.inkcollector_marginy"]
old-location: tablet\inkcollector_marginy.htm
tech.root: tablet
ms.assetid: 6cba076e-6392-4f0a-a80d-3df903d0ba13
ms.date: 12/05/2018
ms.keywords: 6cba076e-6392-4f0a-a80d-3df903d0ba13, IInkCollector interface [Tablet PC],MarginY property, IInkCollector.MarginY, IInkCollector.put_MarginY, IInkCollector::MarginY, IInkCollector::get_MarginY, IInkCollector::put_MarginY, InkCollector.get_MarginY, InkCollector.put_MarginY, MarginY property [Tablet PC], MarginY property [Tablet PC],IInkCollector interface, msinkaut/IInkCollector::MarginY, msinkaut/IInkCollector::get_MarginY, msinkaut/IInkCollector::put_MarginY, put_MarginY, tablet.inkcollector_marginy
f1_keywords:
- msinkaut/IInkCollector.MarginY
dev_langs:
- c++
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
- IInkCollector.MarginY
- IInkCollector.get_MarginY
- IInkCollector.put_MarginY
- InkCollector.get_MarginY
- InkCollector.put_MarginY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector::put_MarginY


## -description



Gets or sets the y-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.



This property is read/write.


## -parameters


## -remarks



This property is most commonly used with nonintegrated tablet devices-the buffer gives users a margin of error when writing on a device that may not map 1 to 1 with the screen.

The margin is specified in screen coordinates. A positive margin extends outside the context, a negative margin extends inside the context, and a value of zero produces no margin. Ink is collected if the stroke starts within the margin. This behavior does not clip the ink. The context of the object or control is either the window input rectangle from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle">GetWindowInputRectangle</a> method or the client rectangle for the window.

The margin is effective only within the application's window. If the pen is applied outside the application's window, then the application loses focus and cannot collect ink.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> object, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. To disable inking in the <b>InkOverlay</b> control, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. You can then set the <b>MarginY</b> property, and re-enable the object or control by setting the <b>Enabled</b> property (or <b>InkEnabled</b> property) to <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx">MarginX Property</a>
 

 

