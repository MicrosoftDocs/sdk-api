---
UID: NF:msinkaut.IInkRecognitionAlternate.get_ConfidenceAlternates
title: IInkRecognitionAlternate::get_ConfidenceAlternates (msinkaut.h)
description: Gets the collection of alternates in which each alternate in the collection consists of the segments with the same property values.
helpviewer_keywords: ["ConfidenceAlternates property [Tablet PC]","ConfidenceAlternates property [Tablet PC]","IInkRecognitionAlternate interface","IInkRecognitionAlternate interface [Tablet PC]","ConfidenceAlternates property","IInkRecognitionAlternate.ConfidenceAlternates","IInkRecognitionAlternate.get_ConfidenceAlternates","IInkRecognitionAlternate::ConfidenceAlternates","IInkRecognitionAlternate::get_ConfidenceAlternates","ef3ab614-7aff-4660-bb2a-783f14e75b94","get_ConfidenceAlternates","msinkaut/IInkRecognitionAlternate::ConfidenceAlternates","msinkaut/IInkRecognitionAlternate::get_ConfidenceAlternates","tablet.iinkrecognitionalternate_confidencealternates"]
old-location: tablet\iinkrecognitionalternate_confidencealternates.htm
tech.root: tablet
ms.assetid: ef3ab614-7aff-4660-bb2a-783f14e75b94
ms.date: 12/05/2018
ms.keywords: ConfidenceAlternates property [Tablet PC], ConfidenceAlternates property [Tablet PC],IInkRecognitionAlternate interface, IInkRecognitionAlternate interface [Tablet PC],ConfidenceAlternates property, IInkRecognitionAlternate.ConfidenceAlternates, IInkRecognitionAlternate.get_ConfidenceAlternates, IInkRecognitionAlternate::ConfidenceAlternates, IInkRecognitionAlternate::get_ConfidenceAlternates, ef3ab614-7aff-4660-bb2a-783f14e75b94, get_ConfidenceAlternates, msinkaut/IInkRecognitionAlternate::ConfidenceAlternates, msinkaut/IInkRecognitionAlternate::get_ConfidenceAlternates, tablet.iinkrecognitionalternate_confidencealternates
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
 - IInkRecognitionAlternate::get_ConfidenceAlternates
 - msinkaut/IInkRecognitionAlternate::get_ConfidenceAlternates
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
 - IInkRecognitionAlternate.ConfidenceAlternates
 - IInkRecognitionAlternate.get_ConfidenceAlternates
 - IInkRecognitionAlternate.get_ConfidenceAlternates
---

# IInkRecognitionAlternate::get_ConfidenceAlternates


## -description

Gets the collection of alternates in which each alternate in the collection consists of the segments with the same property values.



This property is read-only.

## -parameters

## -remarks

This property is an alternative to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method. For more information about properties of alternates, see the <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> constants.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates">LineAlternates Property</a>



<a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty Constants</a>