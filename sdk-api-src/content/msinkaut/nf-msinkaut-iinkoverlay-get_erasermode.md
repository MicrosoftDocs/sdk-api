---
UID: NF:msinkaut.IInkOverlay.get_EraserMode
title: IInkOverlay::get_EraserMode (msinkaut.h)
description: Gets or sets the value that specifies whether ink is erased by stroke or by point. (Get)
helpviewer_keywords: ["87dfd750-254a-4829-b5a2-04aee9890dd0","EraserMode property [Tablet PC]","EraserMode property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","EraserMode property","IInkOverlay.EraserMode","IInkOverlay.get_EraserMode","IInkOverlay::EraserMode","IInkOverlay::get_EraserMode","IInkOverlay::put_EraserMode","InkOverlay.get_EraserMode","InkOverlay.put_EraserMode","get_EraserMode","msinkaut/IInkOverlay::EraserMode","msinkaut/IInkOverlay::get_EraserMode","msinkaut/IInkOverlay::put_EraserMode","tablet.inkoverlay_erasermode"]
old-location: tablet\inkoverlay_erasermode.htm
tech.root: tablet
ms.assetid: 87dfd750-254a-4829-b5a2-04aee9890dd0
ms.date: 12/05/2018
ms.keywords: 87dfd750-254a-4829-b5a2-04aee9890dd0, EraserMode property [Tablet PC], EraserMode property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],EraserMode property, IInkOverlay.EraserMode, IInkOverlay.get_EraserMode, IInkOverlay::EraserMode, IInkOverlay::get_EraserMode, IInkOverlay::put_EraserMode, InkOverlay.get_EraserMode, InkOverlay.put_EraserMode, get_EraserMode, msinkaut/IInkOverlay::EraserMode, msinkaut/IInkOverlay::get_EraserMode, msinkaut/IInkOverlay::put_EraserMode, tablet.inkoverlay_erasermode
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
 - IInkOverlay::get_EraserMode
 - msinkaut/IInkOverlay::get_EraserMode
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
 - IInkOverlay.EraserMode
 - IInkOverlay.get_EraserMode
 - IInkOverlay.put_EraserMode
 - InkOverlay.get_EraserMode
 - InkOverlay.put_EraserMode
---

# IInkOverlay::get_EraserMode


## -description

Gets or sets the value that specifies whether ink is erased by stroke or by point.



This property is read/write.

## -parameters

## -remarks

This property only applies when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode</a> property is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">IOEM_Delete</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode Property [InkOverlay Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">InkOverlayEditingMode Enumeration</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode">InkOverlayEraserMode Enumeration</a>
