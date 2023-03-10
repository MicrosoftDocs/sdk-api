---
UID: NF:msinkaut.IInkRecognizer.get_Languages
title: IInkRecognizer::get_Languages (msinkaut.h)
description: Gets an array of language identifiers for the languages that the IInkRecognizer object supports.
helpviewer_keywords: ["96419ffa-6af1-4e45-a831-f11564501975","IInkRecognizer interface [Tablet PC]","Languages property","IInkRecognizer.Languages","IInkRecognizer.get_Languages","IInkRecognizer::Languages","IInkRecognizer::get_Languages","Languages property [Tablet PC]","Languages property [Tablet PC]","IInkRecognizer interface","get_Languages","msinkaut/IInkRecognizer::Languages","msinkaut/IInkRecognizer::get_Languages","tablet.iinkrecognizer_languages"]
old-location: tablet\iinkrecognizer_languages.htm
tech.root: tablet
ms.assetid: 96419ffa-6af1-4e45-a831-f11564501975
ms.date: 12/05/2018
ms.keywords: 96419ffa-6af1-4e45-a831-f11564501975, IInkRecognizer interface [Tablet PC],Languages property, IInkRecognizer.Languages, IInkRecognizer.get_Languages, IInkRecognizer::Languages, IInkRecognizer::get_Languages, Languages property [Tablet PC], Languages property [Tablet PC],IInkRecognizer interface, get_Languages, msinkaut/IInkRecognizer::Languages, msinkaut/IInkRecognizer::get_Languages, tablet.iinkrecognizer_languages
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
 - IInkRecognizer::get_Languages
 - msinkaut/IInkRecognizer::get_Languages
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
 - IInkRecognizer.Languages
 - IInkRecognizer.get_Languages
 - IInkRecognizer.get_Languages
---

# IInkRecognizer::get_Languages


## -description

Gets an array of language identifiers for the languages that the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object supports.



This property is read-only.

## -parameters

## -remarks

This property can be used to search the <a href="/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)">InkRecognizers</a> collection for a <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> that supports a specific language.

This property returns the empty array for Microsoft gesture recognizer.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name">Name Property</a>