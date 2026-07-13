---
UID: NF:winml.IWinMLRuntime.EvaluateModel
title: IWinMLRuntime::EvaluateModel (winml.h)
description: Evaluates a WinML model.
helpviewer_keywords: ["EvaluateModel","EvaluateModel method","EvaluateModel method","IWinMLRuntime interface","IWinMLRuntime interface","EvaluateModel method","IWinMLRuntime.EvaluateModel","IWinMLRuntime::EvaluateModel","MachineLearning.iwinmlruntime_evaluatemodel","winml/IWinMLRuntime::EvaluateModel"]
old-location: machinelearning\iwinmlruntime_evaluatemodel.htm
tech.root: MachineLearning
ms.assetid: F96A1CCD-02BD-4E93-830D-9975A03658E2
ms.date: 12/05/2018
ms.keywords: EvaluateModel, EvaluateModel method, EvaluateModel method,IWinMLRuntime interface, IWinMLRuntime interface,EvaluateModel method, IWinMLRuntime.EvaluateModel, IWinMLRuntime::EvaluateModel, MachineLearning.iwinmlruntime_evaluatemodel, winml/IWinMLRuntime::EvaluateModel
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
 - IWinMLRuntime::EvaluateModel
 - winml/IWinMLRuntime::EvaluateModel
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
 - IWinMLRuntime.EvaluateModel
---

# IWinMLRuntime::EvaluateModel


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Evaluates a WinML model.

## -parameters

### -param pContext [in]

A pointer to the <a href="/windows/desktop/api/winml/nn-winml-iwinmlevaluationcontext">WinMLEvaluationContext</a> to evaluate.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlruntime">IWinMLRuntime</a>