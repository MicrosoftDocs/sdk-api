---
UID: NE:msinkaut.InkRecognitionConfidence
title: InkRecognitionConfidence (msinkaut.h)
description: Indicates the level of confidence that the recognizer has in the recognition result.
helpviewer_keywords: ["IRC_Intermediate","IRC_Poor","IRC_Strong","InkRecognitionConfidence","InkRecognitionConfidence enumeration [Tablet PC]","ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d","msinkaut/IRC_Intermediate","msinkaut/IRC_Poor","msinkaut/IRC_Strong","msinkaut/InkRecognitionConfidence","tablet.inkrecognitionconfidence"]
old-location: tablet\inkrecognitionconfidence.htm
tech.root: tablet
ms.assetid: ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d
ms.date: 12/05/2018
ms.keywords: IRC_Intermediate, IRC_Poor, IRC_Strong, InkRecognitionConfidence, InkRecognitionConfidence enumeration [Tablet PC], ce99de84-d1c9-420f-8eb5-a8e4f3c04d1d, msinkaut/IRC_Intermediate, msinkaut/IRC_Poor, msinkaut/IRC_Strong, msinkaut/InkRecognitionConfidence, tablet.inkrecognitionconfidence
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
targetos: Windows
req.typenames: InkRecognitionConfidence
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkRecognitionConfidence
 - msinkaut/InkRecognitionConfidence
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRecognitionConfidence
---

# InkRecognitionConfidence enumeration


## -description

Indicates the level of confidence that the recognizer has in the recognition result.

## -enum-fields

### -field IRC_Strong:0

The recognizer is confident that the best recognition alternate is correct.

### -field IRC_Intermediate:1

The recognizer is confident that the correct result is in the list of alternates.

### -field IRC_Poor:2

The recognizer is not confident that the result is in the list of alternates.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence">Confidence Property [IInkGesture Interface]</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topconfidence">TopConfidence Property [IInkRecognitionResult Interface]</a>
