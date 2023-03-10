---
UID: NF:winml.IWinMLEvaluationContext.GetValueByName
title: IWinMLEvaluationContext::GetValueByName (winml.h)
description: Returns the input/output description for the specific binding name.
helpviewer_keywords: ["GetValueByName","GetValueByName method","GetValueByName method","IWinMLEvaluationContext interface","IWinMLEvaluationContext interface","GetValueByName method","IWinMLEvaluationContext.GetValueByName","IWinMLEvaluationContext::GetValueByName","MachineLearning.iwinmlevaluationcontext_getvaluebyname","winml/IWinMLEvaluationContext::GetValueByName"]
old-location: machinelearning\iwinmlevaluationcontext_getvaluebyname.htm
tech.root: MachineLearning
ms.assetid: 750A799F-A5A7-48D2-958B-D03423C0CE09
ms.date: 12/05/2018
ms.keywords: GetValueByName, GetValueByName method, GetValueByName method,IWinMLEvaluationContext interface, IWinMLEvaluationContext interface,GetValueByName method, IWinMLEvaluationContext.GetValueByName, IWinMLEvaluationContext::GetValueByName, MachineLearning.iwinmlevaluationcontext_getvaluebyname, winml/IWinMLEvaluationContext::GetValueByName
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
 - IWinMLEvaluationContext::GetValueByName
 - winml/IWinMLEvaluationContext::GetValueByName
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
 - IWinMLEvaluationContext.GetValueByName
---

# IWinMLEvaluationContext::GetValueByName


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Returns the input/output description for the specific binding name.

## -parameters

### -param Name [in]

The name of the binding.

### -param pDescriptor [out]

A pointer to a <a href="/windows/desktop/api/winml/ns-winml-winml_binding_desc">WINML_BINDING_DESC</a> containing the specified (Name) binding description.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlevaluationcontext">IWinMLEvaluationContext</a>