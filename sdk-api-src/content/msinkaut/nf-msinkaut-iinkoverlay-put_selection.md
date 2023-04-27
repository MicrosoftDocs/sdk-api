---
UID: NF:msinkaut.IInkOverlay.put_Selection
title: IInkOverlay::put_Selection (msinkaut.h)
description: Gets or sets the InkStrokes collection that is currently selected inside the InkOverlay object or the InkPicture control. (Put)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","Selection property","IInkOverlay.Selection","IInkOverlay.put_Selection","IInkOverlay::Selection","IInkOverlay::get_Selection","IInkOverlay::put_Selection","InkOverlay.get_Selection","InkOverlay.put_Selection","Selection property [Tablet PC]","Selection property [Tablet PC]","IInkOverlay interface","fed95f40-d0c4-43a3-9d15-ce9d4d573b5c","msinkaut/IInkOverlay::Selection","msinkaut/IInkOverlay::get_Selection","msinkaut/IInkOverlay::put_Selection","put_Selection","tablet.inkoverlay_selection"]
old-location: tablet\inkoverlay_selection.htm
tech.root: tablet
ms.assetid: fed95f40-d0c4-43a3-9d15-ce9d4d573b5c
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],Selection property, IInkOverlay.Selection, IInkOverlay.put_Selection, IInkOverlay::Selection, IInkOverlay::get_Selection, IInkOverlay::put_Selection, InkOverlay.get_Selection, InkOverlay.put_Selection, Selection property [Tablet PC], Selection property [Tablet PC],IInkOverlay interface, fed95f40-d0c4-43a3-9d15-ce9d4d573b5c, msinkaut/IInkOverlay::Selection, msinkaut/IInkOverlay::get_Selection, msinkaut/IInkOverlay::put_Selection, put_Selection, tablet.inkoverlay_selection
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
 - IInkOverlay::put_Selection
 - msinkaut/IInkOverlay::put_Selection
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
 - IInkOverlay.Selection
 - IInkOverlay.get_Selection
 - IInkOverlay.put_Selection
 - InkOverlay.get_Selection
 - InkOverlay.put_Selection
---

# IInkOverlay::put_Selection


## -description

Gets or sets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection that is currently selected inside the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.



This property is read/write.

## -parameters

## -remarks

To get the bounding rectangle of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection after it has been moved or resized, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox">GetBoundingBox</a> method of the InkStrokes collection returned by this property.

To get the bounding rectangle of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection before it was moved, handle the <a href="/windows/desktop/tablet/inkoverlay-selectionmoved">InkOverlay</a> or the <a href="/windows/desktop/tablet/inkpicture-selectionmoved">InkPicture</a> event.

To get the bounding rectangle of the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection before it was resized, handle the <a href="/windows/desktop/tablet/inkoverlay-selectionresized">InkOverlay</a> or the <a href="/windows/desktop/tablet/inkpicture-selectionresized">InkPicture</a> event.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="/windows/desktop/tablet/inkpicture-selectionmoved">SelectionMoved Event [InkPicture Control]</a>



<a href="/windows/desktop/tablet/inkpicture-selectionresized">SelectionResized Event [InkPicture Control]</a>
