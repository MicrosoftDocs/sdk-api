---
UID: NF:msinkaut.IInkPicture.HitTestSelection
title: IInkPicture::HitTestSelection (msinkaut.h)
description: Retrieves a member of the SelectionHitResult enumeration, which specifies which part of a selection, if any, was hit during a hit test.
helpviewer_keywords: ["8dc745d8-7e2a-4255-86c6-226bf82d3d64","HitTestSelection","HitTestSelection method [Tablet PC]","HitTestSelection method [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","HitTestSelection method","IInkPicture.HitTestSelection","IInkPicture::HitTestSelection","msinkaut/IInkPicture::HitTestSelection","tablet.inkpicture_hittestselection"]
old-location: tablet\inkpicture_hittestselection.htm
tech.root: tablet
ms.assetid: 8dc745d8-7e2a-4255-86c6-226bf82d3d64
ms.date: 12/05/2018
ms.keywords: 8dc745d8-7e2a-4255-86c6-226bf82d3d64, HitTestSelection, HitTestSelection method [Tablet PC], HitTestSelection method [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],HitTestSelection method, IInkPicture.HitTestSelection, IInkPicture::HitTestSelection, msinkaut/IInkPicture::HitTestSelection, tablet.inkpicture_hittestselection
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
 - IInkPicture::HitTestSelection
 - msinkaut/IInkPicture::HitTestSelection
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
 - IInkPicture.HitTestSelection
---

# IInkPicture::HitTestSelection


## -description

Retrieves a member of the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult">SelectionHitResult</a> enumeration, which specifies which part of a selection, if any, was hit during a hit test.

## -parameters

### -param x [in]

The x-position, in pixels, of the hit test.

### -param y [in]

The y-position, in pixels, of the hit test.

### -param SelArea [out]

The value from the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult">SelectionHitResult</a> enumeration.

## -remarks

For further details about this method, refer to the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection">HitTestSelection</a> method, which has the same functionality.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult">SelectionHitResult Enumeration</a>
