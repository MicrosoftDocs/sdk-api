---
UID: NF:msinkaut.IInkRecognizerContext.get_SuffixText
title: IInkRecognizerContext::get_SuffixText (msinkaut.h)
description: Gets or sets the characters that come after the InkStrokes collection in the InkRecognizerContext object. (Get)
helpviewer_keywords: ["IInkRecognizerContext interface [Tablet PC]","SuffixText property","IInkRecognizerContext.SuffixText","IInkRecognizerContext.get_SuffixText","IInkRecognizerContext::SuffixText","IInkRecognizerContext::get_SuffixText","IInkRecognizerContext::put_SuffixText","InkRecognizerContext.get_SuffixText","InkRecognizerContext.put_SuffixText","SuffixText property [Tablet PC]","SuffixText property [Tablet PC]","IInkRecognizerContext interface","f7fb1314-b5d5-4aa9-91d0-cbd649aded39","get_SuffixText","msinkaut/IInkRecognizerContext::SuffixText","msinkaut/IInkRecognizerContext::get_SuffixText","msinkaut/IInkRecognizerContext::put_SuffixText","put_SuffixText","tablet.inkrecognizercontext_suffixtext"]
old-location: tablet\inkrecognizercontext_suffixtext.htm
tech.root: tablet
ms.assetid: f7fb1314-b5d5-4aa9-91d0-cbd649aded39
ms.date: 12/05/2018
ms.keywords: IInkRecognizerContext interface [Tablet PC],SuffixText property, IInkRecognizerContext.SuffixText, IInkRecognizerContext.get_SuffixText, IInkRecognizerContext::SuffixText, IInkRecognizerContext::get_SuffixText, IInkRecognizerContext::put_SuffixText, InkRecognizerContext.get_SuffixText, InkRecognizerContext.put_SuffixText, SuffixText property [Tablet PC], SuffixText property [Tablet PC],IInkRecognizerContext interface, f7fb1314-b5d5-4aa9-91d0-cbd649aded39, get_SuffixText, msinkaut/IInkRecognizerContext::SuffixText, msinkaut/IInkRecognizerContext::get_SuffixText, msinkaut/IInkRecognizerContext::put_SuffixText, put_SuffixText, tablet.inkrecognizercontext_suffixtext
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
 - IInkRecognizerContext::get_SuffixText
 - msinkaut/IInkRecognizerContext::get_SuffixText
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
 - IInkRecognizerContext.SuffixText
 - IInkRecognizerContext.get_SuffixText
 - IInkRecognizerContext.put_SuffixText
 - InkRecognizerContext.get_SuffixText
 - InkRecognizerContext.put_SuffixText
---

# IInkRecognizerContext::get_SuffixText


## -description

Gets or sets the characters that come after the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.



This property is read/write.

## -parameters

## -remarks

The suffix helps improve recognition results by supplying the recognizer with more context about the handwriting.

Setting the <b>SuffixText</b> property succeeds only if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a> property is <b>NULL</b>. You must set the <b>SuffixText</b> property before you attach an <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to the <b>Strokes</b> property of the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a>, or you must set the <b>Strokes</b> property to <b>NULL</b> and then set the <b>SuffixText</b> property.

<div class="alert"><b>Note</b>  If you use the latter method, you may need to reattach the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a> property of the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.</div>
<div> </div>
Setting the <b>SuffixText</b> property to <b>NULL</b> removes any suffix text from the recognizer context.

The suffix text is ignored unless you have set both the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes">Coerce</a> and <b>WordMode</b><b>InkRecognitionModes</b> flags in the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags</a> property.

The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext">PrefixText</a> property gets or sets the characters that come before the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object and also helps improve the recognition result.

If your application provides a correction interface when converting ink to text, the application may allow the user to select characters within a word and use the stylus to generate replacement characters. Your application can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext">PrefixText</a> and <b>SuffixText</b> properties to improve recognition of the new ink.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext">PrefixText Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags Property</a>



<a href="/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes Property</a>
