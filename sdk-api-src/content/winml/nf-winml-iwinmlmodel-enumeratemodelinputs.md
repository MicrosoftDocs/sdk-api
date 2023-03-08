---
UID: NF:winml.IWinMLModel.EnumerateModelInputs
title: IWinMLModel::EnumerateModelInputs (winml.h)
description: Enumerates the WinML model inputs.
helpviewer_keywords: ["EnumerateModelInputs","EnumerateModelInputs method","EnumerateModelInputs method","IWinMLModel interface","IWinMLModel interface","EnumerateModelInputs method","IWinMLModel.EnumerateModelInputs","IWinMLModel::EnumerateModelInputs","MachineLearning.iwinmlmodel_enumeratemodelinputs","winml/IWinMLModel::EnumerateModelInputs"]
old-location: machinelearning\iwinmlmodel_enumeratemodelinputs.htm
tech.root: MachineLearning
ms.assetid: A87B24B0-9463-4022-9054-08F3D7BA5034
ms.date: 12/05/2018
ms.keywords: EnumerateModelInputs, EnumerateModelInputs method, EnumerateModelInputs method,IWinMLModel interface, IWinMLModel interface,EnumerateModelInputs method, IWinMLModel.EnumerateModelInputs, IWinMLModel::EnumerateModelInputs, MachineLearning.iwinmlmodel_enumeratemodelinputs, winml/IWinMLModel::EnumerateModelInputs
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
 - IWinMLModel::EnumerateModelInputs
 - winml/IWinMLModel::EnumerateModelInputs
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
 - IWinMLModel.EnumerateModelInputs
---

# IWinMLModel::EnumerateModelInputs


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Enumerates the WinML model inputs.

## -parameters

### -param Index

Input index value.

### -param ppInputDescriptor [out]

A pointer to a <a href="/windows/desktop/api/winml/ns-winml-winml_variable_desc">WINML_VARIABLE_DESC</a> containing the model input description.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlmodel">IWinMLModel</a>