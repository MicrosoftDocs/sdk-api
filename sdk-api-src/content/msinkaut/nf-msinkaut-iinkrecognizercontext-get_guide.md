---
UID: NF:msinkaut.IInkRecognizerContext.get_Guide
title: IInkRecognizerContext::get_Guide (msinkaut.h)
description: Gets or sets the InkRecognizerGuide to use for ink input. (IInkRecognizerContext.get_Guide)
helpviewer_keywords: ["706d28c3-fc5d-496a-a957-daf5ba8d47ca","Guide property [Tablet PC]","Guide property [Tablet PC]","IInkRecognizerContext interface","IInkRecognizerContext interface [Tablet PC]","Guide property","IInkRecognizerContext.Guide","IInkRecognizerContext.get_Guide","IInkRecognizerContext::Guide","IInkRecognizerContext::get_Guide","IInkRecognizerContext::putref_Guide","InkRecognizerContext.get_Guide","get_Guide","msinkaut/IInkRecognizerContext::Guide","msinkaut/IInkRecognizerContext::get_Guide","msinkaut/IInkRecognizerContext::putref_Guide","putref_Guide","tablet.inkrecognizercontext_guide"]
old-location: tablet\inkrecognizercontext_guide.htm
tech.root: tablet
ms.assetid: 706d28c3-fc5d-496a-a957-daf5ba8d47ca
ms.date: 12/05/2018
ms.keywords: 706d28c3-fc5d-496a-a957-daf5ba8d47ca, Guide property [Tablet PC], Guide property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],Guide property, IInkRecognizerContext.Guide, IInkRecognizerContext.get_Guide, IInkRecognizerContext::Guide, IInkRecognizerContext::get_Guide, IInkRecognizerContext::putref_Guide, InkRecognizerContext.get_Guide, get_Guide, msinkaut/IInkRecognizerContext::Guide, msinkaut/IInkRecognizerContext::get_Guide, msinkaut/IInkRecognizerContext::putref_Guide, putref_Guide, tablet.inkrecognizercontext_guide
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
 - IInkRecognizerContext::get_Guide
 - msinkaut/IInkRecognizerContext::get_Guide
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
 - IInkRecognizerContext.Guide
 - IInkRecognizerContext.get_Guide
 - InkRecognizerContext.get_Guide
---

# IInkRecognizerContext::get_Guide


## -description

Gets or sets the <a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> to use for ink input.



This property is read/write.

## -parameters

## -remarks

Setting the <b>Guide</b> property succeeds only if the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection is <b>NULL</b>. You must set the <b>Guide</b> property before you attach the InkStrokes collection to the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> or you must set the InkStrokes collection to <b>NULL</b> and then set the <b>Guide</b> (and possible reattach the InkStrokes collection).

The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">InkRecognizerCapabilities</a> enumeration contains the <b>IRC_FreeInput</b>, <b>IRC_LinedInput</b>, and <b>IRC_BoxedInput</b> flags. These flags specify the capabilities of a recognizer, but because they are read only, there is no way to set any of these directly on a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> or <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object. The only way to put a recognizer into a specific mode is to set the guide using the <b>Guide</b> property. If you do not set the <b>Guide</b> property, the recognizer defaults to <b>FreeInput</b> mode (if the recognizer is capable of this). Another way to set the recognizer into <b>FreeInput</b> mode is to set the <b>Guide</b> property to a <a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> object that has its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns</a> property set to zero and its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows">Rows</a> property set to zero.

If you set the <b>Guide</b> property to a <a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> object that has its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns</a> property set to zero and its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows">Rows</a> property set to 1 or more, the recognizer is in <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">IRC_LinedInput</a> mode (if the recognizer is capable of this). The recognizer uses the <b>Rows</b> property to control the number of lines.

If you set the <b>Guide</b> property to a <a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> object that has its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows">Rows</a> property set to zero and its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns</a> property set to 1 or more, the recognizer is in <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">IRC_LinedInput</a> mode (if the recognizer is capable of this) for vertical writing. The recognizer uses the <b>Columns</b> property to control the number of vertical lines. If the recognizer is capable of this, the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities</a> property returns either <b>IRC_DownAndLeft</b> or <b>IRC_DownAndRight</b>, or both.

If you set the <b>Guide</b> property to a <a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide</a> object that has its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns</a> property set to 1 or more and its <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows">Rows</a> property set to 1 or more, the recognizer is in <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">IRC_BoxedInput</a> mode (if the recognizer is capable of this).

If you set the mode to one that is not available from this recognizer, an error is returned.

For information about how to query which capabilities, or modes, are available from a specific recognizer, see the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities</a> property of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object. In general, recognizers of Latin script support free input and horizontal lined input, recognizers of East Asian characters support free input and boxed input, and the gesture recognizer only supports free input.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns">Columns Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">InkRecognizerCapabilities Enumeration</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/windows/desktop/tablet/inkrecognizerguide-class">InkRecognizerGuide Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows">Rows Property</a>
