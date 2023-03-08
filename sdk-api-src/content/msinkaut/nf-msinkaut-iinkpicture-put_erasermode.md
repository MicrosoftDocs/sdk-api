---
UID: NF:msinkaut.IInkPicture.put_EraserMode
title: IInkPicture::put_EraserMode (msinkaut.h)
description: Gets or sets a value that specifies whether ink is erased by stroke or by point. (Put)
helpviewer_keywords: ["EraserMode property [Tablet PC]","EraserMode property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","EraserMode property","IInkPicture.EraserMode","IInkPicture.put_EraserMode","IInkPicture::EraserMode","IInkPicture::get_EraserMode","IInkPicture::put_EraserMode","InkPicture.get_EraserMode","InkPicture.put_EraserMode","f6471163-8209-4dd0-887c-0edd54ebb50e","get_EraserMode","msinkaut/IInkPicture::EraserMode","msinkaut/IInkPicture::get_EraserMode","msinkaut/IInkPicture::put_EraserMode","put_EraserMode","tablet.inkpicture_erasermode"]
old-location: tablet\inkpicture_erasermode.htm
tech.root: tablet
ms.assetid: f6471163-8209-4dd0-887c-0edd54ebb50e
ms.date: 12/05/2018
ms.keywords: EraserMode property [Tablet PC], EraserMode property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],EraserMode property, IInkPicture.EraserMode, IInkPicture.put_EraserMode, IInkPicture::EraserMode, IInkPicture::get_EraserMode, IInkPicture::put_EraserMode, InkPicture.get_EraserMode, InkPicture.put_EraserMode, f6471163-8209-4dd0-887c-0edd54ebb50e, get_EraserMode, msinkaut/IInkPicture::EraserMode, msinkaut/IInkPicture::get_EraserMode, msinkaut/IInkPicture::put_EraserMode, put_EraserMode, tablet.inkpicture_erasermode
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
 - IInkPicture::put_EraserMode
 - msinkaut/IInkPicture::put_EraserMode
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
 - IInkPicture.EraserMode
 - IInkPicture.get_EraserMode
 - IInkPicture.put_EraserMode
 - InkPicture.get_EraserMode
 - InkPicture.put_EraserMode
---

# IInkPicture::put_EraserMode


## -description

Gets or sets a value that specifies whether ink is erased by stroke or by point.



This property is read/write.

## -parameters

## -remarks

This property applies only when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode">EditingMode</a> property is set to Delete.

For further details about this property, refer to the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode">EraserMode</a> property, which has the same functionality.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
