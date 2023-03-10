---
UID: NF:msinkaut.IInkPicture.get_CollectingInk
title: IInkPicture::get_CollectingInk (msinkaut.h)
description: Gets a value that specifies whether ink is currently being drawn on an ink collector (InkCollector, InkOverlay, or InkPicture). (IInkPicture.get_CollectingInk)
helpviewer_keywords: ["CollectingInk property [Tablet PC]","CollectingInk property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","CollectingInk property","IInkPicture.CollectingInk","IInkPicture.get_CollectingInk","IInkPicture::CollectingInk","IInkPicture::get_CollectingInk","InkPicture.get_CollectingInk","get_CollectingInk","msinkaut/IInkPicture::CollectingInk","msinkaut/IInkPicture::get_CollectingInk","tablet.inkpicture_collectingink"]
old-location: tablet\inkpicture_collectingink.htm
tech.root: tablet
ms.assetid: 19fbe26e-02a4-4d05-a2e8-25d2f8ae1146
ms.date: 12/05/2018
ms.keywords: CollectingInk property [Tablet PC], CollectingInk property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],CollectingInk property, IInkPicture.CollectingInk, IInkPicture.get_CollectingInk, IInkPicture::CollectingInk, IInkPicture::get_CollectingInk, InkPicture.get_CollectingInk, get_CollectingInk, msinkaut/IInkPicture::CollectingInk, msinkaut/IInkPicture::get_CollectingInk, tablet.inkpicture_collectingink
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
 - IInkPicture::get_CollectingInk
 - msinkaut/IInkPicture::get_CollectingInk
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
 - IInkPicture.CollectingInk
 - IInkPicture.get_CollectingInk
 - InkPicture.get_CollectingInk
---

# IInkPicture::get_CollectingInk


## -description

Gets a value that specifies whether ink is currently being drawn on an ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>).



This property is read-only.

## -parameters

## -remarks

You can use the <b>CollectingInk</b> property to see if ink is being drawn on an ink collector rather than monitoring the <a href="/windows/desktop/tablet/inkpicture-stroke">Stroke</a> event.

<div class="alert"><b>Note</b>  Because ink collection is happening on a different thread than your application code, it is possible that the <b>CollectingInk</b> property can change soon after you have checked it. Thus, your code may be operating under the assumption that the ink collector is not collecting ink, when in fact it is. If this occurs, an error is thrown. To be safe, put such code in a try-catch block.</div>
<div> </div>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
