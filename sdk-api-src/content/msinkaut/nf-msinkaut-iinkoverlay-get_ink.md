---
UID: NF:msinkaut.IInkOverlay.get_Ink
title: IInkOverlay::get_Ink (msinkaut.h)
description: Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. (IInkOverlay.get_Ink)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","Ink property","IInkOverlay.Ink","IInkOverlay.get_Ink","IInkOverlay::Ink","IInkOverlay::get_Ink","IInkOverlay::put_Ink","Ink property [Tablet PC]","Ink property [Tablet PC]","IInkOverlay interface","InkOverlay.get_Ink","InkOverlay.put_Ink","get_Ink","msinkaut/IInkOverlay::Ink","msinkaut/IInkOverlay::get_Ink","msinkaut/IInkOverlay::put_Ink","put_Ink","tablet.inkoverlay_ink"]
old-location: tablet\inkoverlay_ink.htm
tech.root: tablet
ms.assetid: 66b7e5fd-c20b-465d-80dd-31d4d714d00d
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],Ink property, IInkOverlay.Ink, IInkOverlay.get_Ink, IInkOverlay::Ink, IInkOverlay::get_Ink, IInkOverlay::put_Ink, Ink property [Tablet PC], Ink property [Tablet PC],IInkOverlay interface, InkOverlay.get_Ink, InkOverlay.put_Ink, get_Ink, msinkaut/IInkOverlay::Ink, msinkaut/IInkOverlay::get_Ink, msinkaut/IInkOverlay::put_Ink, put_Ink, tablet.inkoverlay_ink
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
 - IInkOverlay::get_Ink
 - msinkaut/IInkOverlay::get_Ink
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
 - IInkOverlay.Ink
 - IInkOverlay.get_Ink
 - IInkOverlay.put_Ink
 - InkOverlay.get_Ink
 - InkOverlay.put_Ink
---

# IInkOverlay::get_Ink


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or an <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> object or the <b>InkOverlay</b> object, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. You can then set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink</a> property, and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
An <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> creates an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object by default. If two or more <b>InkDisp</b> objects exist on a known application window, they can be switched out to enable collection into any of them (such as after deserializing one of the <b>InkDisp</b> objects).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
