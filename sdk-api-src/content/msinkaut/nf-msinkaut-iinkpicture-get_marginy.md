---
UID: NF:msinkaut.IInkPicture.get_MarginY
title: IInkPicture::get_MarginY (msinkaut.h)
description: Gets or sets the y-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window.helpviewer_keywords: ["IInkPicture interface [Tablet PC]","MarginY property","IInkPicture.MarginY","IInkPicture.get_MarginY","IInkPicture::MarginY","IInkPicture::get_MarginY","IInkPicture::put_MarginY","InkPicture.get_MarginY","InkPicture.put_MarginY","MarginY property [Tablet PC]","MarginY property [Tablet PC]","IInkPicture interface","get_MarginY","msinkaut/IInkPicture::MarginY","msinkaut/IInkPicture::get_MarginY","msinkaut/IInkPicture::put_MarginY","put_MarginY","tablet.inkpicture_marginy"]
old-location: tablet\inkpicture_marginy.htm
tech.root: tablet
ms.assetid: f5320061-36c7-4dcb-b5d3-3df41ddcac2a
ms.date: 12/05/2018
ms.keywords: IInkPicture interface [Tablet PC],MarginY property, IInkPicture.MarginY, IInkPicture.get_MarginY, IInkPicture::MarginY, IInkPicture::get_MarginY, IInkPicture::put_MarginY, InkPicture.get_MarginY, InkPicture.put_MarginY, MarginY property [Tablet PC], MarginY property [Tablet PC],IInkPicture interface, get_MarginY, msinkaut/IInkPicture::MarginY, msinkaut/IInkPicture::get_MarginY, msinkaut/IInkPicture::put_MarginY, put_MarginY, tablet.inkpicture_marginy
f1_keywords:
- msinkaut/IInkPicture.MarginY
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
- IInkPicture.MarginY
- IInkPicture.get_MarginY
- IInkPicture.put_MarginY
- InkPicture.get_MarginY
- InkPicture.put_MarginY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkPicture::get_MarginY


## -description



Gets or sets the y-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.



This property is read/write.


## -parameters


## -remarks



This property is most commonly used with nonintegrated tablet devices-the buffer gives users a margin of error when writing on a device that may not map 1 to 1 with the screen.

The margin is specified in screen coordinates. A positive margin extends outside the context, a negative margin extends inside the context, and a value of zero produces no margin. Ink is collected if the stroke starts within the margin. This behavior does not clip the ink. The context of the object or control is either the window input rectangle from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle">GetWindowInputRectangle</a> method or the client rectangle for the window.

The margin is effective only within the application's window. If the pen is applied outside the application's window, then the application loses focus and cannot collect ink.

<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> object, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a> property to <b>FALSE</b>. To disable inking in the <b>InkOverlay</b> control, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. You can then set the <b>MarginY</b> property, and re-enable the object or control by setting the <b>Enabled</b> property (or <b>InkEnabled</b> property) to <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled Property</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx">MarginX Property</a>
 

 

