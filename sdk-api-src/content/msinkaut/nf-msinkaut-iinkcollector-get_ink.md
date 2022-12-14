---
UID: NF:msinkaut.IInkCollector.get_Ink
title: IInkCollector::get_Ink (msinkaut.h)
description: Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object. (IInkCollector.get_Ink)
helpviewer_keywords: ["62881a0e-3932-49a1-8e7d-3e74474f2214","IInkCollector interface [Tablet PC]","Ink property","IInkCollector.Ink","IInkCollector.get_Ink","IInkCollector::Ink","IInkCollector::get_Ink","IInkCollector::putref_Ink","Ink property [Tablet PC]","Ink property [Tablet PC]","IInkCollector interface","InkCollector.get_Ink","get_Ink","msinkaut/IInkCollector::Ink","msinkaut/IInkCollector::get_Ink","msinkaut/IInkCollector::putref_Ink","putref_Ink","tablet.inkcollector_ink"]
old-location: tablet\inkcollector_ink.htm
tech.root: tablet
ms.assetid: 62881a0e-3932-49a1-8e7d-3e74474f2214
ms.date: 12/05/2018
ms.keywords: 62881a0e-3932-49a1-8e7d-3e74474f2214, IInkCollector interface [Tablet PC],Ink property, IInkCollector.Ink, IInkCollector.get_Ink, IInkCollector::Ink, IInkCollector::get_Ink, IInkCollector::putref_Ink, Ink property [Tablet PC], Ink property [Tablet PC],IInkCollector interface, InkCollector.get_Ink, get_Ink, msinkaut/IInkCollector::Ink, msinkaut/IInkCollector::get_Ink, msinkaut/IInkCollector::putref_Ink, putref_Ink, tablet.inkcollector_ink
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
 - IInkCollector::get_Ink
 - msinkaut/IInkCollector::get_Ink
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
 - IInkCollector.Ink
 - IInkCollector.get_Ink
 - get_Ink
 - IInkCollector.get_Ink
 - InkCollector.get_Ink
---

# IInkCollector::get_Ink


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or an <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> object or the <b>InkOverlay</b> object, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. You can then set the <b>Ink</b> property, and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
An <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> creates an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object by default. If two or more <b>InkDisp</b> objects exist on a known application window, they can be switched out to enable collection into any of them (such as after deserializing one of the <b>InkDisp</b> objects).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
