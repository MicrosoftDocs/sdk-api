---
UID: NF:msinkaut.IInkRecognitionAlternate.get_LineAlternates
title: IInkRecognitionAlternate::get_LineAlternates (msinkaut.h)
description: Gets the IInkRecognitionAlternates collection in which each alternate in the collection is on a separate line.
helpviewer_keywords: ["IInkRecognitionAlternate interface [Tablet PC]","LineAlternates property","IInkRecognitionAlternate.LineAlternates","IInkRecognitionAlternate.get_LineAlternates","IInkRecognitionAlternate::LineAlternates","IInkRecognitionAlternate::get_LineAlternates","LineAlternates property [Tablet PC]","LineAlternates property [Tablet PC]","IInkRecognitionAlternate interface","ccdf3092-b0a0-4626-b614-164548b1ca72","get_LineAlternates","msinkaut/IInkRecognitionAlternate::LineAlternates","msinkaut/IInkRecognitionAlternate::get_LineAlternates","tablet.iinkrecognitionalternate_linealternates"]
old-location: tablet\iinkrecognitionalternate_linealternates.htm
tech.root: tablet
ms.assetid: ccdf3092-b0a0-4626-b614-164548b1ca72
ms.date: 12/05/2018
ms.keywords: IInkRecognitionAlternate interface [Tablet PC],LineAlternates property, IInkRecognitionAlternate.LineAlternates, IInkRecognitionAlternate.get_LineAlternates, IInkRecognitionAlternate::LineAlternates, IInkRecognitionAlternate::get_LineAlternates, LineAlternates property [Tablet PC], LineAlternates property [Tablet PC],IInkRecognitionAlternate interface, ccdf3092-b0a0-4626-b614-164548b1ca72, get_LineAlternates, msinkaut/IInkRecognitionAlternate::LineAlternates, msinkaut/IInkRecognitionAlternate::get_LineAlternates, tablet.iinkrecognitionalternate_linealternates
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
 - IInkRecognitionAlternate::get_LineAlternates
 - msinkaut/IInkRecognitionAlternate::get_LineAlternates
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
 - IInkRecognitionAlternate.LineAlternates
 - IInkRecognitionAlternate.get_LineAlternates
 - IInkRecognitionAlternate.get_LineAlternates
---

# IInkRecognitionAlternate::get_LineAlternates


## -description

Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates</a> collection in which each alternate in the collection is on a separate line.



This property is read-only.

## -parameters

## -remarks

If you have a recognition alternate for a paragraph of ink, you can use the <b>LineAlternates</b> property to get a collection of recognition alternates in which each alternate represents a separate line of the paragraph.

This property is an alternative to calling the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues</a> method with the <i>propertyType</i> parameter set to the <a href="/windows/desktop/tablet/recognitionproperty-constants">LineNumber</a> value of the RecognitionProperty constants. For more information about properties of alternates see the RecognitionProperty constants.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object automatically determines the line metrics when drawing ink.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates">ConfidenceAlternates Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates">IInkRecognitionAlternates Interface</a>



<a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty Constants</a>