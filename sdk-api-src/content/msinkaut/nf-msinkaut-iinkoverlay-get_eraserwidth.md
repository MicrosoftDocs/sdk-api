---
UID: NF:msinkaut.IInkOverlay.get_EraserWidth
title: IInkOverlay::get_EraserWidth (msinkaut.h)
description: Gets or sets the value that specifies the width of the eraser pen tip. (Get)
helpviewer_keywords: ["EraserWidth property [Tablet PC]","EraserWidth property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","EraserWidth property","IInkOverlay.EraserWidth","IInkOverlay.get_EraserWidth","IInkOverlay::EraserWidth","IInkOverlay::get_EraserWidth","IInkOverlay::put_EraserWidth","InkOverlay.get_EraserWidth","InkOverlay.put_EraserWidth","d6200640-cf51-44d8-be5a-9dfa5ac36dbc","get_EraserWidth","msinkaut/IInkOverlay::EraserWidth","msinkaut/IInkOverlay::get_EraserWidth","msinkaut/IInkOverlay::put_EraserWidth","put_EraserWidth","tablet.inkoverlay_eraserwidth"]
old-location: tablet\inkoverlay_eraserwidth.htm
tech.root: tablet
ms.assetid: d6200640-cf51-44d8-be5a-9dfa5ac36dbc
ms.date: 12/05/2018
ms.keywords: EraserWidth property [Tablet PC], EraserWidth property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],EraserWidth property, IInkOverlay.EraserWidth, IInkOverlay.get_EraserWidth, IInkOverlay::EraserWidth, IInkOverlay::get_EraserWidth, IInkOverlay::put_EraserWidth, InkOverlay.get_EraserWidth, InkOverlay.put_EraserWidth, d6200640-cf51-44d8-be5a-9dfa5ac36dbc, get_EraserWidth, msinkaut/IInkOverlay::EraserWidth, msinkaut/IInkOverlay::get_EraserWidth, msinkaut/IInkOverlay::put_EraserWidth, put_EraserWidth, tablet.inkoverlay_eraserwidth
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
 - IInkOverlay::get_EraserWidth
 - msinkaut/IInkOverlay::get_EraserWidth
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
 - IInkOverlay.EraserWidth
 - IInkOverlay.get_EraserWidth
 - IInkOverlay.put_EraserWidth
 - InkOverlay.get_EraserWidth
 - InkOverlay.put_EraserWidth
---

# IInkOverlay::get_EraserWidth


## -description

Gets or sets the value that specifies the width of the eraser pen tip.



This property is read/write.

## -parameters

## -remarks

The value specifies the width of the eraser pen tip in ink space units.

You cannot assign negative values to this property.

This property applies only when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode</a> property is set to <b>IOEM_Delete</b> and the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode">EraserMode</a> property is set to <b>IOERM_PointErase</b>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode Property [InkOverlay Class]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode">EraserMode Property [InkOverlay Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">InkOverlayEditingMode Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode">InkOverlayEraserMode Enumeration</a>
