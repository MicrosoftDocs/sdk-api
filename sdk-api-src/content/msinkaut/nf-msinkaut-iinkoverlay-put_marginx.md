---
UID: NF:msinkaut.IInkOverlay.put_MarginX
title: IInkOverlay::put_MarginX
author: windows-sdk-content
description: Gets or sets the x-axis margin around the window rectangle, in screen coordinates.This margin provides a buffer around the edge of the ink window.
old-location: tablet\inkoverlay_marginx.htm
old-project: tablet
ms.assetid: 869fc2dc-ef9b-4427-a7e0-9a2b41b66fe8
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IInkOverlay interface [Tablet PC],MarginX property, IInkOverlay.MarginX, IInkOverlay.put_MarginX, IInkOverlay::MarginX, IInkOverlay::get_MarginX, IInkOverlay::put_MarginX, InkOverlay.get_MarginX, InkOverlay.put_MarginX, MarginX property [Tablet PC], MarginX property [Tablet PC],IInkOverlay interface, get_MarginX, msinkaut/IInkOverlay::MarginX, msinkaut/IInkOverlay::get_MarginX, msinkaut/IInkOverlay::put_MarginX, put_MarginX, tablet.inkoverlay_marginx
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
 - IInkOverlay.MarginX
 - IInkOverlay.get_MarginX
 - IInkOverlay.put_MarginX
 - InkOverlay.get_MarginX
 - InkOverlay.put_MarginX
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::put_MarginX


## -description



Gets or sets the x-axis margin around the window rectangle, in screen coordinates.

This margin provides a buffer around the edge of the ink window.



This property is read/write.


## -parameters


## -remarks



This property is most commonly used with nonintegrated tablet devices?the buffer gives users a margin of error when writing on a device that may not map 1 to 1 with the screen.

The margin is specified in screen coordinates. A positive margin extends outside the context, a negative margin extends inside the context, and a value of zero produces no margin. Ink is collected if the stroke starts within the margin. This behavior does not clip the ink. The context of the object or control is either the window input rectangle from the <a href="https://msdn.microsoft.com/0f47b4c7-7ba1-44a6-8f62-9e97c318bd2c">GetWindowInputRectangle</a> method or the client rectangle for the window.

The margin is effective only within the application's window. If the pen is applied outside the application's window, then the application loses focus and cannot collect ink.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> object, set the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property to <b>FALSE</b>. To disable inking in the <b>InkOverlay</b> control, set the <a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled</a> property to <b>FALSE</b>. You can then set the <a href="https://msdn.microsoft.com/d128fb84-f3cb-4e10-8764-ccb060841383">MarginX</a> property, and re-enable the object or control by setting the <b>Enabled</b> property (or <b>InkEnabled</b> property) to <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/3af59de9-0239-47ab-b3b3-1f1baecb169f">InkEnabled Property</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/6cba076e-6392-4f0a-a80d-3df903d0ba13">MarginY Property</a>
 

 

