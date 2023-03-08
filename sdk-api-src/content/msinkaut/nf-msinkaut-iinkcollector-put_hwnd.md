---
UID: NF:msinkaut.IInkCollector.put_hWnd
title: IInkCollector::put_hWnd (msinkaut.h)
description: Gets or sets the handle value of the window on which ink is drawn. (IInkCollector.put_hWnd)
helpviewer_keywords: ["1a8b933f-a4f0-46f5-8b41-df89b6378e9f","IInkCollector interface [Tablet PC]","hWnd property","IInkCollector.hWnd","IInkCollector.put_hWnd","IInkCollector::get_hWnd","IInkCollector::hWnd","IInkCollector::put_hWnd","InkCollector.get_hWnd","InkCollector.put_hWnd","get_hWnd","hWnd property [Tablet PC]","hWnd property [Tablet PC]","IInkCollector interface","msinkaut/IInkCollector::get_hWnd","msinkaut/IInkCollector::hWnd","msinkaut/IInkCollector::put_hWnd","put_hWnd","tablet.inkcollector_hwnd"]
old-location: tablet\inkcollector_hwnd.htm
tech.root: tablet
ms.assetid: 1a8b933f-a4f0-46f5-8b41-df89b6378e9f
ms.date: 12/05/2018
ms.keywords: 1a8b933f-a4f0-46f5-8b41-df89b6378e9f, IInkCollector interface [Tablet PC],hWnd property, IInkCollector.hWnd, IInkCollector.put_hWnd, IInkCollector::get_hWnd, IInkCollector::hWnd, IInkCollector::put_hWnd, InkCollector.get_hWnd, InkCollector.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],IInkCollector interface, msinkaut/IInkCollector::get_hWnd, msinkaut/IInkCollector::hWnd, msinkaut/IInkCollector::put_hWnd, put_hWnd, tablet.inkcollector_hwnd
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
 - IInkCollector::put_hWnd
 - msinkaut/IInkCollector::put_hWnd
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
 - IInkCollector.hWnd
 - IInkCollector.get_hWnd
 - IInkCollector.put_hWnd
 - put_hWnd
 - IInkCollector.put_hWnd
 - InkCollector.get_hWnd
 - InkCollector.put_hWnd
---

# IInkCollector::put_hWnd


## -description

Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.

## -parameters

## -remarks

If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. You can then set the <b>hWnd</b> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
In Automation, this property is called <b>hWnd Property</b>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
