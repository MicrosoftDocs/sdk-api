---
UID: NN:msinkaut.IInkStrokeDisp
title: IInkStrokeDisp (msinkaut.h)
description: Represents a single ink stroke.A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark.
helpviewer_keywords: ["IInkStrokeDisp","IInkStrokeDisp interface [Tablet PC]","IInkStrokeDisp interface [Tablet PC]","described","b18464ba-feb6-4bb5-9fcf-82feff9bcce4","msinkaut/IInkStrokeDisp","tablet.iinkstrokedisp"]
old-location: tablet\iinkstrokedisp.htm
tech.root: tablet
ms.assetid: b18464ba-feb6-4bb5-9fcf-82feff9bcce4
ms.date: 12/05/2018
ms.keywords: IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], IInkStrokeDisp interface [Tablet PC],described, b18464ba-feb6-4bb5-9fcf-82feff9bcce4, msinkaut/IInkStrokeDisp, tablet.iinkstrokedisp
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
 - IInkStrokeDisp
 - msinkaut/IInkStrokeDisp
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
 - IInkStrokeDisp
---

# IInkStrokeDisp interface


## -description

Represents a single ink stroke.

A stroke is a set of properties and point data that the digitizer captures that represent the coordinates and properties of a known ink mark. It is the set of data that is captured in a single pen down, up, or move sequence.

## -inheritance

The <b>IInkStrokeDisp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkStrokeDisp</b> also has these types of members:

## -remarks

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
