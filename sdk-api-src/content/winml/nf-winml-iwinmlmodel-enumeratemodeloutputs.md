---
UID: NF:winml.IWinMLModel.EnumerateModelOutputs
title: IWinMLModel::EnumerateModelOutputs (winml.h)

description: Enumerates the WinML model outputs.
old-location: machinelearning\iwinmlmodel_enumeratemodeloutputs.htm
tech.root: MachineLearning
ms.assetid: F946AF8E-67BE-4F4B-9BE3-2142CE646B0B

ms.date: 12/05/2018
ms.keywords: EnumerateModelOutputs, EnumerateModelOutputs method, EnumerateModelOutputs method,IWinMLModel interface, IWinMLModel interface,EnumerateModelOutputs method, IWinMLModel.EnumerateModelOutputs, IWinMLModel::EnumerateModelOutputs, MachineLearning.iwinmlmodel_enumeratemodeloutputs, winml/IWinMLModel::EnumerateModelOutputs
ms.topic: method
f1_keywords: 
 - "winml/IWinMLModel.EnumerateModelOutputs"
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
 - IWinMLModel.EnumerateModelOutputs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLModel::EnumerateModelOutputs


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Enumerates the WinML model outputs.


## -parameters




### -param Index [in]

Output index value.


### -param ppOutputDescriptor [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winml/ns-winml-winml_variable_desc">WINML_VARIABLE_DESC</a> containing the model output description.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winml/nn-winml-iwinmlmodel">IWinMLModel</a>
 

 

