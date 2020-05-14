---
UID: NF:winml.IWinMLRuntime.CreateEvaluationContext
title: IWinMLRuntime::CreateEvaluationContext (winml.h)
description: Creates a WinML evaluation context object.helpviewer_keywords: ["CreateEvaluationContext","CreateEvaluationContext method","CreateEvaluationContext method","IWinMLRuntime interface","IWinMLRuntime interface","CreateEvaluationContext method","IWinMLRuntime.CreateEvaluationContext","IWinMLRuntime::CreateEvaluationContext","MachineLearning.iwinmlruntime_createevaluationcontext","winml/IWinMLRuntime::CreateEvaluationContext"]
old-location: machinelearning\iwinmlruntime_createevaluationcontext.htm
tech.root: MachineLearning
ms.assetid: 629D49AF-0AD9-4741-9A59-4B83F521723A
ms.date: 12/05/2018
ms.keywords: CreateEvaluationContext, CreateEvaluationContext method, CreateEvaluationContext method,IWinMLRuntime interface, IWinMLRuntime interface,CreateEvaluationContext method, IWinMLRuntime.CreateEvaluationContext, IWinMLRuntime::CreateEvaluationContext, MachineLearning.iwinmlruntime_createevaluationcontext, winml/IWinMLRuntime::CreateEvaluationContext
f1_keywords:
- winml/IWinMLRuntime.CreateEvaluationContext
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- winml.dll
api_name:
- IWinMLRuntime.CreateEvaluationContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLRuntime::CreateEvaluationContext


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Creates a WinML evaluation context object.


## -parameters




### -param device [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> describing a D3D12 device input.


### -param ppContext [out]

On success, returns a double pointer to the newly-created <a href="https://docs.microsoft.com/windows/desktop/api/winml/nn-winml-iwinmlevaluationcontext">WinMLEvaluationContext</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winml/nn-winml-iwinmlruntime">IWinMLRuntime</a>
 

 

