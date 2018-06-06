---
UID: NF:winml.IWinMLModel.GetDescription
title: IWinMLModel::GetDescription
author: windows-sdk-content
description: Retrieves the WinML model description.
old-location: machinelearning\iwinmlmodel_getdescription.htm
old-project: MachineLearning
ms.assetid: 57B05316-8E6B-4490-B181-EB1717B15E31
ms.author: windowssdkdev
ms.date: 03/07/2018
ms.keywords: GetDescription, GetDescription method, GetDescription method,IWinMLModel interface, IWinMLModel interface,GetDescription method, IWinMLModel.GetDescription, IWinMLModel::GetDescription, MachineLearning.iwinmlmodel_getdescription, winml/IWinMLModel::GetDescription
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
 - IWinMLModel.GetDescription
product: Windows
targetos: Windows
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWinMLModel::GetDescription


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Retrieves the WinML model description.


## -parameters




### -param ppDescription [out]

A pointer to a <a href="https://msdn.microsoft.com/2EDFB412-0EE2-4CC7-9718-D35A815803B2">WINML_MODEL_DESC</a> containing the model description.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/604ABFCC-9CA0-409D-A3FF-D5C59758462E">IWinMLModel</a>
 

 

