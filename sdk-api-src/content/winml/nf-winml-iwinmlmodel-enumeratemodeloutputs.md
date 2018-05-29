---
UID: NF:winml.IWinMLModel.EnumerateModelOutputs
title: IWinMLModel::EnumerateModelOutputs
author: windows-sdk-content
description: Enumerates the WinML model outputs.
old-location: machinelearning\iwinmlmodel_enumeratemodeloutputs.htm
old-project: MachineLearning
ms.assetid: F946AF8E-67BE-4F4B-9BE3-2142CE646B0B
ms.author: windowssdkdev
ms.date: 03/07/2018
ms.keywords: EnumerateModelOutputs, EnumerateModelOutputs method, EnumerateModelOutputs method,IWinMLModel interface, IWinMLModel interface,EnumerateModelOutputs method, IWinMLModel.EnumerateModelOutputs, IWinMLModel::EnumerateModelOutputs, MachineLearning.iwinmlmodel_enumeratemodeloutputs, winml/IWinMLModel::EnumerateModelOutputs
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
req.typenames: WINML_TENSOR_DATA_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winml.dll
api_name:
-	IWinMLModel.EnumerateModelOutputs
product: Windows
targetos: Windows
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWinMLModel::EnumerateModelOutputs


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Enumerates the WinML model outputs.


## -parameters




### -param Index [in]

Output index value.


### -param ppOutputDescriptor [out]

A pointer to a <a href="https://msdn.microsoft.com/94FBC8E4-13BD-49A5-A720-0827479A43A6">WINML_VARIABLE_DESC</a> containing the model output description.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/604ABFCC-9CA0-409D-A3FF-D5C59758462E">IWinMLModel</a>
 

 

