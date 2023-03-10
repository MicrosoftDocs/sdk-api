---
UID: NN:msinkaut.IInkStrokes
title: IInkStrokes (msinkaut.h)
description: . (IInkStrokes)
helpviewer_keywords: ["IInkStrokes","IInkStrokes interface [Tablet PC]","IInkStrokes interface [Tablet PC]","described","msinkaut/IInkStrokes","tablet.iinkstrokes"]
old-location: tablet\iinkstrokes.htm
tech.root: tablet
ms.assetid: 496234C1-C20B-46FE-A9BB-4B90C14FEB46
ms.date: 12/05/2018
ms.keywords: IInkStrokes, IInkStrokes interface [Tablet PC], IInkStrokes interface [Tablet PC],described, msinkaut/IInkStrokes, tablet.iinkstrokes
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokes
 - msinkaut/IInkStrokes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkStrokes
---

# IInkStrokes interface


## -description

Represents a collection of ink strokes.

A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark. It is the set of data that is captured in a single pen down, up, or move sequence.

## -inheritance

The <b>IInkStrokes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 

## -see-also

[IInkStrokeDisp interface](nn-msinkaut-iinkstrokedisp.md)

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>

<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>

<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
