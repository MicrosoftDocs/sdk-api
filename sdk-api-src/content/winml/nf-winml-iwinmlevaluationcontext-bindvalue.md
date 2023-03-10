---
UID: NF:winml.IWinMLEvaluationContext.BindValue
title: IWinMLEvaluationContext::BindValue (winml.h)
description: Binds the input/output to the given model.
helpviewer_keywords: ["BindValue","BindValue method","BindValue method","IWinMLEvaluationContext interface","IWinMLEvaluationContext interface","BindValue method","IWinMLEvaluationContext.BindValue","IWinMLEvaluationContext::BindValue","MachineLearning.iwinmlevaluationcontext_bindvalue_","winml/IWinMLEvaluationContext::BindValue"]
old-location: machinelearning\iwinmlevaluationcontext_bindvalue_.htm
tech.root: MachineLearning
ms.assetid: 3D417952-92DD-4111-9060-C7F8CCA456AB
ms.date: 12/05/2018
ms.keywords: BindValue, BindValue method, BindValue method,IWinMLEvaluationContext interface, IWinMLEvaluationContext interface,BindValue method, IWinMLEvaluationContext.BindValue, IWinMLEvaluationContext::BindValue, MachineLearning.iwinmlevaluationcontext_bindvalue_, winml/IWinMLEvaluationContext::BindValue
req.header: winml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWinMLEvaluationContext::BindValue
 - winml/IWinMLEvaluationContext::BindValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winml.dll
api_name:
 - IWinMLEvaluationContext.BindValue
---

# IWinMLEvaluationContext::BindValue


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Binds the input/output to the given model.

## -parameters

### -param pDescriptor [in]

A pointer to a <a href="/windows/desktop/api/winml/ns-winml-winml_binding_desc">WINML_BINDING_DESC</a> containing the input/output binding descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlevaluationcontext">IWinMLEvaluationContext</a>