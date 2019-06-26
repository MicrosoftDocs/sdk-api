---
UID: NS:winml.WINML_TENSOR_BINDING_DESC
title: WINML_TENSOR_BINDING_DESC (winml.h)
author: windows-sdk-content
description: Contains description properties of the tensor binding.
old-location: machinelearning\winml_tensor_binding_desc.htm
tech.root: MachineLearning
ms.assetid: A99A57DB-4602-4841-85FF-BC655CAB6C6F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_tensor_binding_desc, PWINML_TENSOR_BINDING_DESC, PWINML_TENSOR_BINDING_DESC structure pointer, WINML_TENSOR_BINDING_DESC, WINML_TENSOR_BINDING_DESC structure, winml/PWINML_TENSOR_BINDING_DESC, winml/WINML_TENSOR_BINDING_DESC
ms.topic: struct
f1_keywords: 
 - "winml/WINML_TENSOR_BINDING_DESC"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winml.h
api_name:
 - WINML_TENSOR_BINDING_DESC
product: Windows
targetos: Windows
req.typenames: WINML_TENSOR_BINDING_DESC
req.redist: 
ms.custom: 19H1
---

# WINML_TENSOR_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains description properties of the tensor binding.


## -struct-fields




### -field DataType

A <a href="https://docs.microsoft.com/windows/desktop/api/winml/ne-winml-winml_tensor_data_type">WINML_TENSOR_DATA_TYPE</a> containing the WinML tensor data type.


### -field NumDimensions

The WinML tensor dimension count.


### -field pShape

A pointer to the shape of the WinML tensor.


### -field DataSize

The size of tensor data in bytes.


### -field pData

Pointer to the tensor data.

