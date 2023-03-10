---
UID: NF:winml.IWinMLModel.GetDescription
title: IWinMLModel::GetDescription (winml.h)
description: Retrieves the WinML model description.
helpviewer_keywords: ["GetDescription","GetDescription method","GetDescription method","IWinMLModel interface","IWinMLModel interface","GetDescription method","IWinMLModel.GetDescription","IWinMLModel::GetDescription","MachineLearning.iwinmlmodel_getdescription","winml/IWinMLModel::GetDescription"]
old-location: machinelearning\iwinmlmodel_getdescription.htm
tech.root: MachineLearning
ms.assetid: 57B05316-8E6B-4490-B181-EB1717B15E31
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method, GetDescription method,IWinMLModel interface, IWinMLModel interface,GetDescription method, IWinMLModel.GetDescription, IWinMLModel::GetDescription, MachineLearning.iwinmlmodel_getdescription, winml/IWinMLModel::GetDescription
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
 - IWinMLModel::GetDescription
 - winml/IWinMLModel::GetDescription
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
 - IWinMLModel.GetDescription
---

# IWinMLModel::GetDescription


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Retrieves the WinML model description.

## -parameters

### -param ppDescription [out]

A pointer to a <a href="/windows/desktop/api/winml/ns-winml-winml_model_desc">WINML_MODEL_DESC</a> containing the model description.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlmodel">IWinMLModel</a>