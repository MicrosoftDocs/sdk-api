---
UID: NF:msinkaut.IInkPicture.get_EraserWidth
title: IInkPicture::get_EraserWidth (msinkaut.h)
description: Gets or sets a value that specifies the width of the eraser pen tip. (Get)
helpviewer_keywords: ["8a880a9a-acd4-4cb1-aea7-4d834ecd9490","EraserWidth property [Tablet PC]","EraserWidth property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","EraserWidth property","IInkPicture.EraserWidth","IInkPicture.get_EraserWidth","IInkPicture::EraserWidth","IInkPicture::get_EraserWidth","IInkPicture::put_EraserWidth","InkPicture.get_EraserWidth","InkPicture.put_EraserWidth","get_EraserWidth","msinkaut/IInkPicture::EraserWidth","msinkaut/IInkPicture::get_EraserWidth","msinkaut/IInkPicture::put_EraserWidth","put_EraserWidth","tablet.inkpicture_eraserwidth"]
old-location: tablet\inkpicture_eraserwidth.htm
tech.root: tablet
ms.assetid: 8a880a9a-acd4-4cb1-aea7-4d834ecd9490
ms.date: 12/05/2018
ms.keywords: 8a880a9a-acd4-4cb1-aea7-4d834ecd9490, EraserWidth property [Tablet PC], EraserWidth property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],EraserWidth property, IInkPicture.EraserWidth, IInkPicture.get_EraserWidth, IInkPicture::EraserWidth, IInkPicture::get_EraserWidth, IInkPicture::put_EraserWidth, InkPicture.get_EraserWidth, InkPicture.put_EraserWidth, get_EraserWidth, msinkaut/IInkPicture::EraserWidth, msinkaut/IInkPicture::get_EraserWidth, msinkaut/IInkPicture::put_EraserWidth, put_EraserWidth, tablet.inkpicture_eraserwidth
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
 - IInkPicture::get_EraserWidth
 - msinkaut/IInkPicture::get_EraserWidth
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
 - IInkPicture.EraserWidth
 - IInkPicture.get_EraserWidth
 - IInkPicture.put_EraserWidth
 - InkPicture.get_EraserWidth
 - InkPicture.put_EraserWidth
---

# IInkPicture::get_EraserWidth


## -description

Gets or sets a value that specifies the width of the eraser pen tip.



This property is read/write.

## -parameters

## -remarks

The value specifies the width of the eraser pen tip in ink space units.

You cannot assign negative values to this property.

This property applies only when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode">EditingMode</a> property is set to <b>IOEM_Delete</b> and the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode">EraserMode</a> property is set to <b>IOERM_PointErase</b>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode">EditingMode [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode">EraserMode [InkPicture Control]</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode">EraserMode Enumeration</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
