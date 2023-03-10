---
UID: NF:msinkaut.IInkOverlay.put_hWnd
title: IInkOverlay::put_hWnd (msinkaut.h)
description: Gets or sets the handle value of the window on which ink is drawn. (IInkOverlay.put_hWnd)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","hWnd property","IInkOverlay.hWnd","IInkOverlay.put_hWnd","IInkOverlay::get_hWnd","IInkOverlay::hWnd","IInkOverlay::put_hWnd","InkOverlay.get_hWnd","InkOverlay.put_hWnd","get_hWnd","hWnd property [Tablet PC]","hWnd property [Tablet PC]","IInkOverlay interface","msinkaut/IInkOverlay::get_hWnd","msinkaut/IInkOverlay::hWnd","msinkaut/IInkOverlay::put_hWnd","put_hWnd","tablet.inkoverlay_hwnd"]
old-location: tablet\inkoverlay_hwnd.htm
tech.root: tablet
ms.assetid: fb08bdb5-4d2e-4a2e-9e23-bbff4cedc6e2
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],hWnd property, IInkOverlay.hWnd, IInkOverlay.put_hWnd, IInkOverlay::get_hWnd, IInkOverlay::hWnd, IInkOverlay::put_hWnd, InkOverlay.get_hWnd, InkOverlay.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],IInkOverlay interface, msinkaut/IInkOverlay::get_hWnd, msinkaut/IInkOverlay::hWnd, msinkaut/IInkOverlay::put_hWnd, put_hWnd, tablet.inkoverlay_hwnd
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
 - IInkOverlay::put_hWnd
 - msinkaut/IInkOverlay::put_hWnd
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
 - IInkOverlay.hWnd
 - IInkOverlay.get_hWnd
 - IInkOverlay.put_hWnd
 - InkOverlay.get_hWnd
 - InkOverlay.put_hWnd
---

# IInkOverlay::put_hWnd


## -description

Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.

## -parameters

## -remarks

If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. You can then set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
In Automation, this property is called <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd Property</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
