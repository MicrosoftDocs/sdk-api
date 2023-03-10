---
UID: NF:peninputpanel.IHandwrittenTextInsertion.InsertInkRecognitionResult
title: IHandwrittenTextInsertion::InsertInkRecognitionResult (peninputpanel.h)
description: Inserts recognition results.
helpviewer_keywords: ["IHandWrittenTextInsertion interface [Tablet PC]","InsertInkRecognitionResult method","IHandWrittenTextInsertion::InsertInkRecognitionResult","IHandwrittenTextInsertion.InsertInkRecognitionResult","IHandwrittenTextInsertion::InsertInkRecognitionResult","InsertInkRecognitionResult","InsertInkRecognitionResult method [Tablet PC]","InsertInkRecognitionResult method [Tablet PC]","IHandWrittenTextInsertion interface","d519aff4-573d-4b06-aef5-e9cc6a5e8102","peninputpanel/IHandWrittenTextInsertion::InsertInkRecognitionResult","tablet.ihandwrittentextinsertion_insertinkrecognitionresult"]
old-location: tablet\ihandwrittentextinsertion_insertinkrecognitionresult.htm
tech.root: tablet
ms.assetid: d519aff4-573d-4b06-aef5-e9cc6a5e8102
ms.date: 12/05/2018
ms.keywords: IHandWrittenTextInsertion interface [Tablet PC],InsertInkRecognitionResult method, IHandWrittenTextInsertion::InsertInkRecognitionResult, IHandwrittenTextInsertion.InsertInkRecognitionResult, IHandwrittenTextInsertion::InsertInkRecognitionResult, InsertInkRecognitionResult, InsertInkRecognitionResult method [Tablet PC], InsertInkRecognitionResult method [Tablet PC],IHandWrittenTextInsertion interface, d519aff4-573d-4b06-aef5-e9cc6a5e8102, peninputpanel/IHandWrittenTextInsertion::InsertInkRecognitionResult, tablet.ihandwrittentextinsertion_insertinkrecognitionresult
req.header: peninputpanel.h
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHandwrittenTextInsertion::InsertInkRecognitionResult
 - peninputpanel/IHandwrittenTextInsertion::InsertInkRecognitionResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - IHandWrittenTextInsertion.InsertInkRecognitionResult
---

# IHandwrittenTextInsertion::InsertInkRecognitionResult


## -description

Inserts recognition results.

## -parameters

### -param pIInkRecoResult [in]

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> for the insertion which contains the recognition results and the collection of ink strokes for the insertion.

### -param locale [in]

The locale identifier of a specific culture for the input language of the recognizer used to produce alternates.

### -param fAlternateContainsAutoSpacingInformation [in]

Specifies whether the recognized text was generated with auto-spacing enabled on the recognized. <b>TRUE</b> if auto-spacing was enabled; otherwise, <b>FALSE</b>.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion">IHandWrittenTextInsertion</a>