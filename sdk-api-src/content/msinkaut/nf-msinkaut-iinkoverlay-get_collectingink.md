---
UID: NF:msinkaut.IInkOverlay.get_CollectingInk
title: IInkOverlay::get_CollectingInk (msinkaut.h)
description: Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). (IInkOverlay.get_CollectingInk)
helpviewer_keywords: ["CollectingInk property [Tablet PC]","CollectingInk property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","CollectingInk property","IInkOverlay.CollectingInk","IInkOverlay.get_CollectingInk","IInkOverlay::CollectingInk","IInkOverlay::get_CollectingInk","InkOverlay.get_CollectingInk","get_CollectingInk","msinkaut/IInkOverlay::CollectingInk","msinkaut/IInkOverlay::get_CollectingInk","tablet.inkoverlay_collectingink"]
old-location: tablet\inkoverlay_collectingink.htm
tech.root: tablet
ms.assetid: fa689979-0c8c-4295-9750-3c2fee9af4d9
ms.date: 12/05/2018
ms.keywords: CollectingInk property [Tablet PC], CollectingInk property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],CollectingInk property, IInkOverlay.CollectingInk, IInkOverlay.get_CollectingInk, IInkOverlay::CollectingInk, IInkOverlay::get_CollectingInk, InkOverlay.get_CollectingInk, get_CollectingInk, msinkaut/IInkOverlay::CollectingInk, msinkaut/IInkOverlay::get_CollectingInk, tablet.inkoverlay_collectingink
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
 - IInkOverlay::get_CollectingInk
 - msinkaut/IInkOverlay::get_CollectingInk
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
 - IInkOverlay.CollectingInk
 - IInkOverlay.get_CollectingInk
 - InkOverlay.get_CollectingInk
---

# IInkOverlay::get_CollectingInk


## -description

Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>).



This property is read-only.

## -parameters

## -remarks

You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property to see if ink is being drawn on an ink collector rather than monitoring the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event.

<div class="alert"><b>Note</b>  Because ink collection is happening on a different thread than your application code, it is possible that the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property can change soon after you have checked it. Thus, your code may be operating under the assumption that the ink collector is not collecting ink, when in fact it is. If this occurs, an error is thrown. To be safe, put such code in a try-catch block.</div>
<div> </div>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
