---
UID: NF:msinkaut.IInkRecognitionResult.get_TopConfidence
title: IInkRecognitionResult::get_TopConfidence (msinkaut.h)
author: windows-sdk-content
description: Gets the top alternate of the recognition result.
old-location: tablet\iinkrecognitionresult_topconfidence.htm
tech.root: tablet
ms.assetid: 286283ca-a8ad-4fc5-ae46-09a3e6382e2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 286283ca-a8ad-4fc5-ae46-09a3e6382e2a, IInkRecognitionResult interface [Tablet PC],TopConfidence property, IInkRecognitionResult.TopConfidence, IInkRecognitionResult.get_TopConfidence, IInkRecognitionResult::TopConfidence, IInkRecognitionResult::get_TopConfidence, TopConfidence property [Tablet PC], TopConfidence property [Tablet PC],IInkRecognitionResult interface, get_TopConfidence, msinkaut/IInkRecognitionResult::TopConfidence, msinkaut/IInkRecognitionResult::get_TopConfidence, tablet.iinkrecognitionresult_topconfidence
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkRecognitionResult.TopConfidence"
dev_langs:
 - c++
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
 - IInkRecognitionResult.TopConfidence
 - IInkRecognitionResult.get_TopConfidence
 - IInkRecognitionResult.get_TopConfidence
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionResult::get_TopConfidence


## -description



Gets the top alternate of the recognition result.



This property is read-only.


## -parameters


## -remarks



Of the Microsoft <b>recognizers</b>, only the Microsoft English (US) Handwriting Recognizer and the Microsoft Gesture Recognizer support confidence levels. Third party recognizers may or may not support confidence levels.

<div class="alert"><b>Note</b>  The <b>TopConfidence</b> property may change if a call to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate</a> method causes a change to the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate</a> property.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence">InkRecognitionConfidence Enumeration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topalternate">TopAlternate Property</a>
 

 

