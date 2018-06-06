---
UID: NF:winml.IWinMLRuntime.CreateEvaluationContext
title: IWinMLRuntime::CreateEvaluationContext
author: windows-sdk-content
description: Creates a WinML evaluation context object.
old-location: machinelearning\iwinmlruntime_createevaluationcontext.htm
old-project: MachineLearning
ms.assetid: 629D49AF-0AD9-4741-9A59-4B83F521723A
ms.author: windowssdkdev
ms.date: 03/07/2018
ms.keywords: CreateEvaluationContext, CreateEvaluationContext method, CreateEvaluationContext method,IWinMLRuntime interface, IWinMLRuntime interface,CreateEvaluationContext method, IWinMLRuntime.CreateEvaluationContext, IWinMLRuntime::CreateEvaluationContext, MachineLearning.iwinmlruntime_createevaluationcontext, winml/IWinMLRuntime::CreateEvaluationContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WINML_TENSOR_DATA_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winml.dll
api_name:
 - IWinMLRuntime.CreateEvaluationContext
product: Windows
targetos: Windows
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWinMLRuntime::CreateEvaluationContext


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Creates a WinML evaluation context object.


## -parameters




### -param device [in]

A pointer to an <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> describing a D3D12 device input.


### -param ppContext [out]

On success, returns a double pointer to the newly-created <a href="https://msdn.microsoft.com/D4C9B16A-B351-41E4-AD42-20C25F3CC404">WinMLEvaluationContext</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C2FD74A1-EE38-46B1-98A8-43557485F92E">IWinMLRuntime</a>
 

 

