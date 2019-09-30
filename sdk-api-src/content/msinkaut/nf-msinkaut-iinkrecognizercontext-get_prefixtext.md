---
UID: NF:msinkaut.IInkRecognizerContext.get_PrefixText
title: IInkRecognizerContext::get_PrefixText (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the characters that come before the InkStrokes collection in the InkRecognizerContext object.
old-location: tablet\inkrecognizercontext_prefixtext.htm
tech.root: tablet
ms.assetid: fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkRecognizerContext interface [Tablet PC],PrefixText property, IInkRecognizerContext.PrefixText, IInkRecognizerContext.get_PrefixText, IInkRecognizerContext::PrefixText, IInkRecognizerContext::get_PrefixText, IInkRecognizerContext::put_PrefixText, InkRecognizerContext.get_PrefixText, InkRecognizerContext.put_PrefixText, PrefixText property [Tablet PC], PrefixText property [Tablet PC],IInkRecognizerContext interface, fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97, get_PrefixText, msinkaut/IInkRecognizerContext::PrefixText, msinkaut/IInkRecognizerContext::get_PrefixText, msinkaut/IInkRecognizerContext::put_PrefixText, put_PrefixText, tablet.inkrecognizercontext_prefixtext
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkRecognizerContext.PrefixText"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerContext.PrefixText
 - IInkRecognizerContext.get_PrefixText
 - IInkRecognizerContext.put_PrefixText
 - InkRecognizerContext.get_PrefixText
 - InkRecognizerContext.put_PrefixText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognizerContext::get_PrefixText


## -description



Gets or sets the characters that come before the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.



This property is read/write.


## -parameters


## -remarks



The prefix helps improve recognition results by supplying the recognizer with more context about the handwriting.

Setting the <b>PrefixText</b> property succeeds only if the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a> property is <b>NULL</b>. You must set the <b>PrefixText</b> property before you attach a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to the <b>Strokes</b> property of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a>, or you must set the <b>Strokes</b> property to <b>NULL</b> and then set the <b>PrefixText</b> property.

<div class="alert"><b>Note</b>  If you use the latter method, you may need to reattach the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes">Strokes</a> property of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.</div>
<div> </div>
Setting the <b>PrefixText</b> property to <b>NULL</b> removes any prefix text from the recognizer context.

The prefix text is ignored unless you have set both the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes">IRM_Coerce</a> and <b>IRM_WordMode</b><b>InkRecognitionModes</b> flags in the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags</a> property.

The <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext">SuffixText</a> property gets or sets the characters that come after the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object and also helps improve the recognition result.

If your application provides a correction interface when converting ink to text, the application may allow the user to select characters within a word and use the stylus to generate replacement characters. Your application can use the <b>PrefixText</b> and <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext">SuffixText</a> properties to improve recognition of the new ink.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes">Strokes Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext">SuffixText Property</a>
 

 

