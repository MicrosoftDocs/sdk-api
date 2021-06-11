---
UID: NF:msinkaut.IInkOverlay.Draw
title: IInkOverlay::Draw (msinkaut.h)
description: Sets a rectangle in which to redraw the ink within the InkOverlay object.
helpviewer_keywords: ["80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb","Draw","Draw method [Tablet PC]","Draw method [Tablet PC]","IInkOverlay interface","IInkOverlay","IInkOverlay interface [Tablet PC]","Draw method","IInkOverlay.Draw","IInkOverlay::Draw","msinkaut/IInkOverlay::Draw","tablet.inkoverlay_draw"]
old-location: tablet\inkoverlay_draw.htm
tech.root: tablet
ms.assetid: 80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb
ms.date: 12/05/2018
ms.keywords: 80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb, Draw, Draw method [Tablet PC], Draw method [Tablet PC],IInkOverlay interface, IInkOverlay, IInkOverlay interface [Tablet PC],Draw method, IInkOverlay.Draw, IInkOverlay::Draw, msinkaut/IInkOverlay::Draw, tablet.inkoverlay_draw
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
 - IInkOverlay::Draw
 - msinkaut/IInkOverlay::Draw
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
 - IInkOverlay.Draw
---

# IInkOverlay::Draw


## -description

Sets a rectangle in which to redraw the ink within the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object.

## -parameters

### -param Rect [in]

The rectangle on which to draw, in pixel coordinates. When this parameter is <b>NULL</b>, the entire window is redrawn.

## -returns

This method can return one of these values.

## -remarks

<a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> within the rectangle represented by <i>rDrawRect</i> is drawn when the area is next repainted if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw</a> property is <b>TRUE</b>.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>
