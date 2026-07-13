---
UID: NF:msinkaut15.IInkDivider.get_RecognizerContext
title: IInkDivider::get_RecognizerContext (msinkaut15.h)
description: Gets or sets the InkRecognizerContext object that the InkDivider object uses for layout analysis. (IInkDivider.get_RecognizerContext)
helpviewer_keywords: ["IInkDivider interface [Tablet PC]","RecognizerContext property","IInkDivider.RecognizerContext","IInkDivider.get_RecognizerContext","IInkDivider::RecognizerContext","IInkDivider::get_RecognizerContext","IInkDivider::putref_RecognizerContext","InkDivider.get_RecognizerContext","RecognizerContext property [Tablet PC]","RecognizerContext property [Tablet PC]","IInkDivider interface","ad3c4317-a777-4009-bc66-865a2fcb77c3","get_RecognizerContext","msinkaut15/IInkDivider::RecognizerContext","msinkaut15/IInkDivider::get_RecognizerContext","msinkaut15/IInkDivider::putref_RecognizerContext","put_RecognizerContext","tablet.inkdivider_recognizercontext"]
old-location: tablet\inkdivider_recognizercontext.htm
tech.root: tablet
ms.assetid: ad3c4317-a777-4009-bc66-865a2fcb77c3
ms.date: 12/05/2018
ms.keywords: IInkDivider interface [Tablet PC],RecognizerContext property, IInkDivider.RecognizerContext, IInkDivider.get_RecognizerContext, IInkDivider::RecognizerContext, IInkDivider::get_RecognizerContext, IInkDivider::putref_RecognizerContext, InkDivider.get_RecognizerContext, RecognizerContext property [Tablet PC], RecognizerContext property [Tablet PC],IInkDivider interface, ad3c4317-a777-4009-bc66-865a2fcb77c3, get_RecognizerContext, msinkaut15/IInkDivider::RecognizerContext, msinkaut15/IInkDivider::get_RecognizerContext, msinkaut15/IInkDivider::putref_RecognizerContext, put_RecognizerContext, tablet.inkdivider_recognizercontext
req.header: msinkaut15.h
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
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDivider::get_RecognizerContext
 - msinkaut15/IInkDivider::get_RecognizerContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivider.RecognizerContext
 - IInkDivider.get_RecognizerContext
 - InkDivider.get_RecognizerContext
---

# IInkDivider::get_RecognizerContext


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object that the <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object uses for layout analysis.



This property is read/write.

## -parameters

## -remarks

If you set the <b>RecognizerContext</b> property, it should be the first thing you do after constructing the <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object. An error is generated if you attempt to set the <b>RecognizerContext</b> property after the <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes">Divider.Strokes</a> property has been set, after a <a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivider-divide">Divider.Divide</a> call has been made, or if you attempt to set it more than one time.

In addition, this property generates an error if you assign a recognizer context to it that:

<ul>
<li>Is not a text recognizer.</li>
<li>Does not free support.</li>
</ul>
If the value of this property is <b>NULL</b> when strokes are assigned to the <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object, then the <b>InkDivider</b> object uses no recognizer context.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkdivider-class">InkDivider</a> object uses the default property settings of the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object, and ignores any strokes assigned to the <b>InkRecognizerContext</b> object.</div>
<div> </div>

## -see-also

<a href="../msinkaut15/nn-msinkaut15-iinkdivider.md">IInkDivider</a>



<a href="/windows/desktop/tablet/inkdivider-class">InkDivider Class</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
