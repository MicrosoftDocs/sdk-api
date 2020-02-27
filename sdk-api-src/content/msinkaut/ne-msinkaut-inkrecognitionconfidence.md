---
UID: NE:msinkaut.InkRecognitionConfidence
title: InkRecognitionConfidence (msinkaut.h)
description: Indicates the level of confidence that the recognizer has in the recognition result.
old-location: tablet\inkrecognitionconfidence.htm
tech.root: tablet
ms.assetid: ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d
ms.date: 12/05/2018
ms.keywords: IRC_Intermediate, IRC_Poor, IRC_Strong, InkRecognitionConfidence, InkRecognitionConfidence enumeration [Tablet PC], ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d, msinkaut/IRC_Intermediate, msinkaut/IRC_Poor, msinkaut/IRC_Strong, msinkaut/InkRecognitionConfidence, tablet.inkrecognitionconfidence
f1_keywords:
- msinkaut/InkRecognitionConfidence
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- msinkaut.h
api_name:
- InkRecognitionConfidence
targetos: Windows
req.typenames: InkRecognitionConfidence
req.redist: 
ms.custom: 19H1
---

# InkRecognitionConfidence enumeration


## -description



Indicates the level of confidence that the recognizer has in the recognition result.




## -enum-fields




### -field IRC_Strong

The recognizer is confident that the best recognition alternate is correct.


### -field IRC_Intermediate

The recognizer is confident that the correct result is in the list of alternates.


### -field IRC_Poor

The recognizer is not confident that the result is in the list of alternates.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence">Confidence Property [IInkGesture Interface]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topconfidence">TopConfidence Property [IInkRecognitionResult Interface]</a>
 

 

