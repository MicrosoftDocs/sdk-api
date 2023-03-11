---
UID: NF:msinkaut.IInkPicture.get_hWnd
title: IInkPicture::get_hWnd (msinkaut.h)
description: Gets or sets the handle value of the window on which ink is drawn. (IInkPicture.get_hWnd)
helpviewer_keywords: ["IInkPicture interface [Tablet PC]","hWnd property","IInkPicture.get_hWnd","IInkPicture.hWnd","IInkPicture::get_hWnd","IInkPicture::hWnd","IInkPicture::put_hWnd","InkPicture.get_hWnd","InkPicture.put_hWnd","get_hWnd","hWnd property [Tablet PC]","hWnd property [Tablet PC]","IInkPicture interface","msinkaut/IInkPicture::get_hWnd","msinkaut/IInkPicture::hWnd","msinkaut/IInkPicture::put_hWnd","put_hWnd","tablet.inkpicture_hwnd"]
old-location: tablet\inkpicture_hwnd.htm
tech.root: tablet
ms.assetid: c11f13f5-f0a8-45f8-83c2-372df670ef1f
ms.date: 12/05/2018
ms.keywords: IInkPicture interface [Tablet PC],hWnd property, IInkPicture.get_hWnd, IInkPicture.hWnd, IInkPicture::get_hWnd, IInkPicture::hWnd, IInkPicture::put_hWnd, InkPicture.get_hWnd, InkPicture.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],IInkPicture interface, msinkaut/IInkPicture::get_hWnd, msinkaut/IInkPicture::hWnd, msinkaut/IInkPicture::put_hWnd, put_hWnd, tablet.inkpicture_hwnd
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
 - IInkPicture::get_hWnd
 - msinkaut/IInkPicture::get_hWnd
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
 - IInkPicture.hWnd
 - IInkPicture.get_hWnd
 - IInkPicture.put_hWnd
 - InkPicture.get_hWnd
 - InkPicture.put_hWnd
---

# IInkPicture::get_hWnd


## -description

Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.

## -parameters

## -remarks

If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>VARIANT_FALSE</b>. You can then set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a> property and re-enable the object by setting the <b>Enabled</b> property to <b>VARIANT_TRUE</b>.</div>
<div> </div>
In Automation, this property is called <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd Property</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
