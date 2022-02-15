---
UID: NN:msinkaut.IInkRecognitionAlternate
title: IInkRecognitionAlternate (msinkaut.h)
description: Represents the possible word matches for segments of ink that are compared to a recognizers dictionary.
helpviewer_keywords: ["219e96ee-6492-4f76-9928-f2e8dc28493d","IInkRecognitionAlternate","IInkRecognitionAlternate interface [Tablet PC]","IInkRecognitionAlternate interface [Tablet PC]","described","msinkaut/IInkRecognitionAlternate","tablet.iinkrecognitionalternate"]
old-location: tablet\iinkrecognitionalternate.htm
tech.root: tablet
ms.assetid: 219e96ee-6492-4f76-9928-f2e8dc28493d
ms.date: 12/05/2018
ms.keywords: 219e96ee-6492-4f76-9928-f2e8dc28493d, IInkRecognitionAlternate, IInkRecognitionAlternate interface [Tablet PC], IInkRecognitionAlternate interface [Tablet PC],described, msinkaut/IInkRecognitionAlternate, tablet.iinkrecognitionalternate
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
 - IInkRecognitionAlternate
 - msinkaut/IInkRecognitionAlternate
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
 - IInkRecognitionAlternate
---

# IInkRecognitionAlternate interface


## -description

Represents the possible word matches for segments of ink that are compared to a recognizers dictionary.

## -inheritance

The <b>IInkRecognitionAlternate</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRecognitionAlternate</b> also has these types of members:

## -remarks

A recognition segment is a basic ink fragment or unit that the recognizer uses internally to produce a recognition result for a known <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. The segments are usually determined by spacing and are broken down into the smallest possible ink fragments.

Sometimes the ink may have ambiguous distinctions between segments. These segments are compared to a recognizer's dictionary to determine possible matches (alternates). When the segments are compared, the recognizer creates a list of possible alternates and assigns a confidence level to each one, picking a top choice.

For instance, consider the phrase "how are you". This phrase is probably broken into three segments (depending on the spacing between segments), one for each word.

When each segment is recognized, a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">RecognitionResult</a> is created. Each result then returns a list of alternates to choose from. For instance, the segment "how" may have alternates like "how", "now", "new", and so on, with "how" being the top alternate. By default, the top alternate is returned for each segment. You can choose to return alternates other than the top alternate.

You can also return alternates that are based on the properties of the alternates, such as the confidence level of the recognition result, the line number on which the alternates appear, and so on. See the <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> object for a list of the recognition properties.

Alternates of alternates can also be returned.

Not all recognizers set all of the properties listed above. When an application attempts to access a property that is not set by the recognizer, an argument exception is thrown.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty Constants</a>
