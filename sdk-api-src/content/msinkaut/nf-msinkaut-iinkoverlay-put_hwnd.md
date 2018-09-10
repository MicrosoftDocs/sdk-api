---
UID: NF:msinkaut.IInkOverlay.put_hWnd
title: IInkOverlay::put_hWnd
author: windows-sdk-content
description: Gets or sets the handle value of the window on which ink is drawn.
old-location: tablet\inkoverlay_hwnd.htm
tech.root: tablet
ms.assetid: fb08bdb5-4d2e-4a2e-9e23-bbff4cedc6e2
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IInkOverlay interface [Tablet PC],hWnd property, IInkOverlay.hWnd, IInkOverlay.put_hWnd, IInkOverlay::get_hWnd, IInkOverlay::hWnd, IInkOverlay::put_hWnd, InkOverlay.get_hWnd, InkOverlay.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],IInkOverlay interface, msinkaut/IInkOverlay::get_hWnd, msinkaut/IInkOverlay::hWnd, msinkaut/IInkOverlay::put_hWnd, put_hWnd, tablet.inkoverlay_hwnd
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
 - IInkOverlay.hWnd
 - IInkOverlay.get_hWnd
 - IInkOverlay.put_hWnd
 - InkOverlay.get_hWnd
 - InkOverlay.put_hWnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::put_hWnd


## -description



Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.


## -parameters


## -remarks



If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled</a> property to <b>FALSE</b>. You can then set the <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
In Automation, this property is called <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd Property</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="https://msdn.microsoft.com/ACE11946-113B-42EE-A3F1-0036B1DF8141">IInkOverlay</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>
 

 

