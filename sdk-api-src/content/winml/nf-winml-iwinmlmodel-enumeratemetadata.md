---
UID: NF:winml.IWinMLModel.EnumerateMetadata
title: IWinMLModel::EnumerateMetadata (winml.h)
description: Gets the metadata of the model.
helpviewer_keywords: ["EnumerateMetadata","EnumerateMetadata method","EnumerateMetadata method","IWinMLModel interface","IWinMLModel interface","EnumerateMetadata method","IWinMLModel.EnumerateMetadata","IWinMLModel::EnumerateMetadata","MachineLearning.iwinmlmodel_enumeratemetadata","winml/IWinMLModel::EnumerateMetadata"]
old-location: machinelearning\iwinmlmodel_enumeratemetadata.htm
tech.root: MachineLearning
ms.assetid: ABB51498-44CE-4B98-89FB-ED8B9B8159ED
ms.date: 12/05/2018
ms.keywords: EnumerateMetadata, EnumerateMetadata method, EnumerateMetadata method,IWinMLModel interface, IWinMLModel interface,EnumerateMetadata method, IWinMLModel.EnumerateMetadata, IWinMLModel::EnumerateMetadata, MachineLearning.iwinmlmodel_enumeratemetadata, winml/IWinMLModel::EnumerateMetadata
f1_keywords:
- winml/IWinMLModel.EnumerateMetadata
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
- IWinMLModel.EnumerateMetadata
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLModel::EnumerateMetadata


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Gets the metadata of the model.


## -parameters




### -param Index [in]

The metadata index value.


### -param pKey [out]

A pointer to the metadata key for the given index.


### -param pValue [out]

A pointer to the metadata value for the given index.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winml/nn-winml-iwinmlmodel">IWinMLModel</a>
 

 

