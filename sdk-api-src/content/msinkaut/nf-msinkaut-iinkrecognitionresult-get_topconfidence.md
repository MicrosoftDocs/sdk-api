---
UID: NF:msinkaut.IInkRecognitionResult.get_TopConfidence
title: IInkRecognitionResult::get_TopConfidence
author: windows-sdk-content
description: Gets the top alternate of the recognition result.
old-location: tablet\iinkrecognitionresult_topconfidence.htm
tech.root: tablet
ms.assetid: 286283ca-a8ad-4fc5-ae46-09a3e6382e2a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 286283ca-a8ad-4fc5-ae46-09a3e6382e2a, IInkRecognitionResult interface [Tablet PC],TopConfidence property, IInkRecognitionResult.TopConfidence, IInkRecognitionResult.get_TopConfidence, IInkRecognitionResult::TopConfidence, IInkRecognitionResult::get_TopConfidence, TopConfidence property [Tablet PC], TopConfidence property [Tablet PC],IInkRecognitionResult interface, get_TopConfidence, msinkaut/IInkRecognitionResult::TopConfidence, msinkaut/IInkRecognitionResult::get_TopConfidence, tablet.iinkrecognitionresult_topconfidence
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkRecognitionResult.get_TopConfidence
: 
---

# IInkRecognitionResult::get_TopConfidence


## -description



Gets the top alternate of the recognition result.



This property is read-only.


## -parameters


## -remarks



Of the Microsoft <b>recognizers</b>, only the Microsoft English (US) Handwriting Recognizer and the Microsoft Gesture Recognizer support confidence levels. Third party recognizers may or may not support confidence levels.

<div class="alert"><b>Note</b>  The <b>TopConfidence</b> property may change if a call to the <a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate</a> method causes a change to the <a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate</a> property.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fd7ee250-6f76-419b-8164-0d2717ea288c">IInkRecognitionResult Interface</a>



<a href="https://msdn.microsoft.com/ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d">InkRecognitionConfidence Enumeration</a>



<a href="https://msdn.microsoft.com/98edc5e9-2388-4f4e-a67f-029ee83be4cb">ModifyTopAlternate Method</a>



<a href="https://msdn.microsoft.com/6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d">TopAlternate Property</a>
 

 

