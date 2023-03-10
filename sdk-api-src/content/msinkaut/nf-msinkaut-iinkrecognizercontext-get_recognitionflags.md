---
UID: NF:msinkaut.IInkRecognizerContext.get_RecognitionFlags
title: IInkRecognizerContext::get_RecognitionFlags (msinkaut.h)
description: Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string. (Get)
helpviewer_keywords: ["71b02f99-4076-4c56-b88a-4201b7033411","IInkRecognizerContext interface [Tablet PC]","RecognitionFlags property","IInkRecognizerContext.RecognitionFlags","IInkRecognizerContext.get_RecognitionFlags","IInkRecognizerContext::RecognitionFlags","IInkRecognizerContext::get_RecognitionFlags","IInkRecognizerContext::put_RecognitionFlags","InkRecognizerContext.get_RecognitionFlags","InkRecognizerContext.put_RecognitionFlags","RecognitionFlags property [Tablet PC]","RecognitionFlags property [Tablet PC]","IInkRecognizerContext interface","get_RecognitionFlags","msinkaut/IInkRecognizerContext::RecognitionFlags","msinkaut/IInkRecognizerContext::get_RecognitionFlags","msinkaut/IInkRecognizerContext::put_RecognitionFlags","put_RecognitionFlags","tablet.inkrecognizercontext_recognitionflags"]
old-location: tablet\inkrecognizercontext_recognitionflags.htm
tech.root: tablet
ms.assetid: 71b02f99-4076-4c56-b88a-4201b7033411
ms.date: 12/05/2018
ms.keywords: 71b02f99-4076-4c56-b88a-4201b7033411, IInkRecognizerContext interface [Tablet PC],RecognitionFlags property, IInkRecognizerContext.RecognitionFlags, IInkRecognizerContext.get_RecognitionFlags, IInkRecognizerContext::RecognitionFlags, IInkRecognizerContext::get_RecognitionFlags, IInkRecognizerContext::put_RecognitionFlags, InkRecognizerContext.get_RecognitionFlags, InkRecognizerContext.put_RecognitionFlags, RecognitionFlags property [Tablet PC], RecognitionFlags property [Tablet PC],IInkRecognizerContext interface, get_RecognitionFlags, msinkaut/IInkRecognizerContext::RecognitionFlags, msinkaut/IInkRecognizerContext::get_RecognitionFlags, msinkaut/IInkRecognizerContext::put_RecognitionFlags, put_RecognitionFlags, tablet.inkrecognizercontext_recognitionflags
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
 - IInkRecognizerContext::get_RecognitionFlags
 - msinkaut/IInkRecognizerContext::get_RecognitionFlags
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
 - IInkRecognizerContext.RecognitionFlags
 - IInkRecognizerContext.get_RecognitionFlags
 - IInkRecognizerContext.put_RecognitionFlags
 - InkRecognizerContext.get_RecognitionFlags
 - InkRecognizerContext.put_RecognitionFlags
---

# IInkRecognizerContext::get_RecognitionFlags


## -description

Gets or sets the flags that specify how the recognizer interprets the ink and determines the result string.



This property is read/write.

## -parameters

## -remarks

The <b>RecognitionFlags</b> property gets or sets flags that specify things such as whether the recognizer treats all ink as a single word or whether the recognizer coerces the result based on the factoid that you specified for the context.

Setting the <b>RecognitionFlags</b> property succeeds only if the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a> property is <b>NULL</b>.

For a list of modes that you can use, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes">InkRecognitionModes</a> enumeration type.

<div class="alert"><b>Note</b>  You can combine modes using the bitwise <b>OR</b> operator.</div>
<div> </div>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes">InkRecognitionModes Enumeration</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
