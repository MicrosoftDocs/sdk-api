---
UID: NF:msinkaut.IInkRecognitionResult.get_TopAlternate
title: IInkRecognitionResult::get_TopAlternate (msinkaut.h)
description: Gets the top alternate of the recognition result.helpviewer_keywords: ["6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d","IInkRecognitionResult interface [Tablet PC]","TopAlternate property","IInkRecognitionResult.TopAlternate","IInkRecognitionResult.get_TopAlternate","IInkRecognitionResult::TopAlternate","IInkRecognitionResult::get_TopAlternate","TopAlternate property [Tablet PC]","TopAlternate property [Tablet PC]","IInkRecognitionResult interface","get_TopAlternate","msinkaut/IInkRecognitionResult::TopAlternate","msinkaut/IInkRecognitionResult::get_TopAlternate","tablet.iinkrecognitionresult_topalternate"]
old-location: tablet\iinkrecognitionresult_topalternate.htm
tech.root: tablet
ms.assetid: 6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d
ms.date: 12/05/2018
ms.keywords: 6be3d9d1-8c59-48c5-a6a5-10d93b47cd5d, IInkRecognitionResult interface [Tablet PC],TopAlternate property, IInkRecognitionResult.TopAlternate, IInkRecognitionResult.get_TopAlternate, IInkRecognitionResult::TopAlternate, IInkRecognitionResult::get_TopAlternate, TopAlternate property [Tablet PC], TopAlternate property [Tablet PC],IInkRecognitionResult interface, get_TopAlternate, msinkaut/IInkRecognitionResult::TopAlternate, msinkaut/IInkRecognitionResult::get_TopAlternate, tablet.iinkrecognitionresult_topalternate
f1_keywords:
- msinkaut/IInkRecognitionResult.TopAlternate
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
- IInkRecognitionResult.TopAlternate
- IInkRecognitionResult.get_TopAlternate
- IInkRecognitionResult.get_TopAlternate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkRecognitionResult::get_TopAlternate


## -description



Gets the top alternate of the recognition result.



This property is read-only.


## -parameters


## -remarks



When the recognizer returns a recognition result, the recognition alternates are ranked from the highest confidence level to the lowest confidence level. The recognition alternate with the highest confidence level is selected as the top alternate.

You can use the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate</a> method to change which recognition alternate is the top alternate.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognitionAlternate Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-modifytopalternate">ModifyTopAlternate Method</a>
 

 

