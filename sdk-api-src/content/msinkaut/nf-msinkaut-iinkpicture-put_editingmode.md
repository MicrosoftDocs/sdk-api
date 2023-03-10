---
UID: NF:msinkaut.IInkPicture.put_EditingMode
title: IInkPicture::put_EditingMode (msinkaut.h)
description: Gets or sets a value that specifies whether the InkPicture control is in ink mode, deletion mode, or selecting/editing mode. (Put)
helpviewer_keywords: ["5767f768-d59c-404e-9098-ab5e0c427c7d","EditingMode property [Tablet PC]","EditingMode property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","EditingMode property","IInkPicture.EditingMode","IInkPicture.put_EditingMode","IInkPicture::EditingMode","IInkPicture::get_EditingMode","IInkPicture::put_EditingMode","InkPicture.get_EditingMode","InkPicture.put_EditingMode","get_EditingMode","msinkaut/IInkPicture::EditingMode","msinkaut/IInkPicture::get_EditingMode","msinkaut/IInkPicture::put_EditingMode","put_EditingMode","tablet.inkpicture_editingmode"]
old-location: tablet\inkpicture_editingmode.htm
tech.root: tablet
ms.assetid: 5767f768-d59c-404e-9098-ab5e0c427c7d
ms.date: 12/05/2018
ms.keywords: 5767f768-d59c-404e-9098-ab5e0c427c7d, EditingMode property [Tablet PC], EditingMode property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],EditingMode property, IInkPicture.EditingMode, IInkPicture.put_EditingMode, IInkPicture::EditingMode, IInkPicture::get_EditingMode, IInkPicture::put_EditingMode, InkPicture.get_EditingMode, InkPicture.put_EditingMode, get_EditingMode, msinkaut/IInkPicture::EditingMode, msinkaut/IInkPicture::get_EditingMode, msinkaut/IInkPicture::put_EditingMode, put_EditingMode, tablet.inkpicture_editingmode
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
 - IInkPicture::put_EditingMode
 - msinkaut/IInkPicture::put_EditingMode
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
 - IInkPicture.EditingMode
 - IInkPicture.get_EditingMode
 - IInkPicture.put_EditingMode
 - InkPicture.get_EditingMode
 - InkPicture.put_EditingMode
---

# IInkPicture::put_EditingMode


## -description

Gets or sets a value that specifies whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.



This property is read/write.

## -parameters

## -remarks

The <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> and <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> objects generate an error if you change the <b>EditingMode</b> property while ink is being collected. To avoid this conflict, make sure the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink">CollectingInk</a> property is <b>FALSE</b> before changing the <b>EditingMode</b> property.

For more information about erasing ink, see <a href="/windows/desktop/tablet/erasing-ink-with-the-pen">Erasing Ink with the Pen</a>.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
