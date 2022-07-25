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
 - IWinMLModel::EnumerateMetadata
 - winml/IWinMLModel::EnumerateMetadata
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
 - IWinMLModel.EnumerateMetadata
---

# IWinMLModel::EnumerateMetadata


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Gets the metadata of the model.

## -parameters

### -param Index [in]

The metadata index value.

### -param pKey [out]

A pointer to the metadata key for the given index.

### -param pValue [out]

A pointer to the metadata value for the given index.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/winml/nn-winml-iwinmlmodel">IWinMLModel</a>