---
UID: NF:msinkaut.IInkRecognitionResult.get_TopString
title: IInkRecognitionResult::get_TopString (msinkaut.h)
description: Gets the result text for the TopAlternate property.
helpviewer_keywords: ["9f345372-0208-4c78-9da7-9b334c0f281e","IInkRecognitionResult interface [Tablet PC]","TopString property","IInkRecognitionResult.TopString","IInkRecognitionResult.get_TopString","IInkRecognitionResult::TopString","IInkRecognitionResult::get_TopString","TopString property [Tablet PC]","TopString property [Tablet PC]","IInkRecognitionResult interface","get_TopString","msinkaut/IInkRecognitionResult::TopString","msinkaut/IInkRecognitionResult::get_TopString","tablet.iinkrecognitionresult_topstring"]
old-location: tablet\iinkrecognitionresult_topstring.htm
tech.root: tablet
ms.assetid: 9f345372-0208-4c78-9da7-9b334c0f281e
ms.date: 12/05/2018
ms.keywords: 9f345372-0208-4c78-9da7-9b334c0f281e, IInkRecognitionResult interface [Tablet PC],TopString property, IInkRecognitionResult.TopString, IInkRecognitionResult.get_TopString, IInkRecognitionResult::TopString, IInkRecognitionResult::get_TopString, TopString property [Tablet PC], TopString property [Tablet PC],IInkRecognitionResult interface, get_TopString, msinkaut/IInkRecognitionResult::TopString, msinkaut/IInkRecognitionResult::get_TopString, tablet.iinkrecognitionresult_topstring
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
 - IInkRecognitionResult::get_TopString
 - msinkaut/IInkRecognitionResult::get_TopString
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
 - IInkRecognitionResult.TopString
 - IInkRecognitionResult.get_TopString
 - IInkRecognitionResult.get_TopString
---

# IInkRecognitionResult::get_TopString


## -description

Gets the result text for the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate</a> property.



This property is read-only.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The result text for the <b>TopString</b> property changes if a call to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate</a> method causes a change to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate</a> property.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate Property</a>