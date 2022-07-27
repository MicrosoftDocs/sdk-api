---
UID: NF:msinkaut.IInkOverlay.put_EditingMode
title: IInkOverlay::put_EditingMode (msinkaut.h)
description: Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode. (Put)
helpviewer_keywords: ["3b734da3-5784-4504-b22e-b86844d42f4e","EditingMode property [Tablet PC]","EditingMode property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","EditingMode property","IInkOverlay.EditingMode","IInkOverlay.put_EditingMode","IInkOverlay::EditingMode","IInkOverlay::get_EditingMode","IInkOverlay::put_EditingMode","InkOverlay.get_EditingMode","InkOverlay.put_EditingMode","get_EditingMode","msinkaut/IInkOverlay::EditingMode","msinkaut/IInkOverlay::get_EditingMode","msinkaut/IInkOverlay::put_EditingMode","put_EditingMode","tablet.inkoverlay_editingmode"]
old-location: tablet\inkoverlay_editingmode.htm
tech.root: tablet
ms.assetid: 3b734da3-5784-4504-b22e-b86844d42f4e
ms.date: 12/05/2018
ms.keywords: 3b734da3-5784-4504-b22e-b86844d42f4e, EditingMode property [Tablet PC], EditingMode property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],EditingMode property, IInkOverlay.EditingMode, IInkOverlay.put_EditingMode, IInkOverlay::EditingMode, IInkOverlay::get_EditingMode, IInkOverlay::put_EditingMode, InkOverlay.get_EditingMode, InkOverlay.put_EditingMode, get_EditingMode, msinkaut/IInkOverlay::EditingMode, msinkaut/IInkOverlay::get_EditingMode, msinkaut/IInkOverlay::put_EditingMode, put_EditingMode, tablet.inkoverlay_editingmode
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
 - IInkOverlay::put_EditingMode
 - msinkaut/IInkOverlay::put_EditingMode
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
 - IInkOverlay.EditingMode
 - IInkOverlay.get_EditingMode
 - IInkOverlay.put_EditingMode
 - InkOverlay.get_EditingMode
 - InkOverlay.put_EditingMode
---

# IInkOverlay::put_EditingMode


## -description

Gets or sets a value that specifies whether the object/control is in ink mode, deletion mode, or selecting/editing mode.



This property is read/write.

## -parameters

## -remarks

The <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> and <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> objects generate an error if you change the <b>EditingMode</b> property while ink is being collected. To avoid this conflict, make sure the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property is <b>FALSE</b> before changing the <b>EditingMode</b> property.

For more information about erasing ink, see <a href="/windows/desktop/tablet/erasing-ink-with-the-pen">Erasing Ink with the Pen</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled Property</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode">InkOverlayEditingMode Enumeration</a>
