---
UID: NF:msinkaut.IInkRecognitionAlternate.get_Confidence
title: IInkRecognitionAlternate::get_Confidence
author: windows-sdk-content
description: Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an IInkRecognitionAlternate object or a gesture.
old-location: tablet\iinkrecognitionalternate_confidence.htm
tech.root: tablet
ms.assetid: 049a5742-fc4f-4a9a-91d5-5eec56dc8e8b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 049a5742-fc4f-4a9a-91d5-5eec56dc8e8b, Confidence property [Tablet PC], Confidence property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],Confidence property, IInkRecognitionAlternate.Confidence, IInkRecognitionAlternate.get_Confidence, IInkRecognitionAlternate::Confidence, IInkRecognitionAlternate::get_Confidence, get_Confidence, msinkaut/IInkRecognitionAlternate::Confidence, msinkaut/IInkRecognitionAlternate::get_Confidence, tablet.iinkrecognitionalternate_confidence
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
 - IInkRecognitionAlternate.Confidence
 - IInkRecognitionAlternate.get_Confidence
 - IInkRecognitionAlternate.get_Confidence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognitionAlternate::get_Confidence


## -description



Gets the level of confidence (strong, intermediate, or poor) that a recognizer has in the recognition of an <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate</a> object or a gesture.



This property is read-only.


## -parameters


## -remarks



For a list of confidence values that may be returned, see the <a href="https://msdn.microsoft.com/ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d">InkRecognitionConfidence</a> enumeration type.

<div class="alert"><b>Note</b>  Confidence evaluation is available for all gesture recognizers in the current release of Windows XP Tablet PC Edition.</div>
<div> </div>

<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a> object:

If the alternate represents a phrase or sentence, the value represents the lowest confidence level of a recognition segment found in the phrase or sentence. However, if the alternate represents a word, the value represents the confidence level of the word.

<div class="alert"><b>Note</b>  This property throws an exception if the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a> that generates the <a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognitionAlternate Interface</a> does not support confidence levels.</div>
<div> </div>
Of the Microsoft recognizers, only the Microsoft English (US) Handwriting Recognizer and the Microsoft Gesture Recognizer support confidence levels. Third party recognizers may or may not support confidence levels.




## -see-also




<a href="https://msdn.microsoft.com/87a1db34-371e-4c02-a470-55f35dfbf4ab">IInkGesture Interface</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognition Alternate Interface</a>



<a href="https://msdn.microsoft.com/ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d">InkRecognitionConfidence Enumeration</a>
 

 

