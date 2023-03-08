---
UID: NF:msinkaut.IInkPicture.get_Ink
title: IInkPicture::get_Ink (msinkaut.h)
description: Gets or sets the InkDisp object that is associated with the InkPicture control.
helpviewer_keywords: ["8a6001bb-cfb9-4c24-8f99-3c8f0acd443c","IInkPicture interface [Tablet PC]","Ink property","IInkPicture.Ink","IInkPicture.get_Ink","IInkPicture::Ink","IInkPicture::get_Ink","IInkPicture::put_Ink","Ink property [Tablet PC]","Ink property [Tablet PC]","IInkPicture interface","InkPicture.get_Ink","InkPicture.put_Ink","get_Ink","get_ink","msinkaut/IInkPicture::Ink","msinkaut/IInkPicture::get_Ink","msinkaut/IInkPicture::put_Ink","putref_ink","tablet.inkpicture_ink"]
old-location: tablet\inkpicture_ink.htm
tech.root: tablet
ms.assetid: 8a6001bb-cfb9-4c24-8f99-3c8f0acd443c
ms.date: 12/05/2018
ms.keywords: 8a6001bb-cfb9-4c24-8f99-3c8f0acd443c, IInkPicture interface [Tablet PC],Ink property, IInkPicture.Ink, IInkPicture.get_Ink, IInkPicture::Ink, IInkPicture::get_Ink, IInkPicture::put_Ink, Ink property [Tablet PC], Ink property [Tablet PC],IInkPicture interface, InkPicture.get_Ink, InkPicture.put_Ink, get_Ink, get_ink, msinkaut/IInkPicture::Ink, msinkaut/IInkPicture::get_Ink, msinkaut/IInkPicture::put_Ink, putref_ink, tablet.inkpicture_ink
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
 - IInkPicture::get_Ink
 - msinkaut/IInkPicture::get_Ink
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
 - IInkPicture.Ink
 - IInkPicture.get_Ink
 - IInkPicture.put_Ink
 - InkPicture.get_Ink
 - InkPicture.put_Ink
---

# IInkPicture::get_Ink


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is associated with the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.



This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control must be disabled before setting this property. To disable inking in the InkPicture control, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. You can then set the <b>Ink</b> property, and re-enable the control by setting the <b>InkEnabled</b> property to <b>TRUE</b>.</div>
<div> </div>
For further details about this property, refer to the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink">Ink</a> property, which has the same functionality.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>
