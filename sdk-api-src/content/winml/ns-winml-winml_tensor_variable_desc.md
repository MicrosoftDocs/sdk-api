---
UID: NS:winml.WINML_TENSOR_VARIABLE_DESC
title: WINML_TENSOR_VARIABLE_DESC (winml.h)
description: Contains description properties of the tensor variable.
helpviewer_keywords: ["MachineLearning.winml_tensor_variable_desc","PWINML_TENSOR_VARIABLE_DESC","PWINML_TENSOR_VARIABLE_DESC structure pointer","WINML_TENSOR_VARIABLE_DESC","WINML_TENSOR_VARIABLE_DESC structure","winml/PWINML_TENSOR_VARIABLE_DESC","winml/WINML_TENSOR_VARIABLE_DESC"]
old-location: machinelearning\winml_tensor_variable_desc.htm
tech.root: MachineLearning
ms.assetid: 71D65FC6-7A2B-40D6-B040-213C8BC77BE0
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_tensor_variable_desc, PWINML_TENSOR_VARIABLE_DESC, PWINML_TENSOR_VARIABLE_DESC structure pointer, WINML_TENSOR_VARIABLE_DESC, WINML_TENSOR_VARIABLE_DESC structure, winml/PWINML_TENSOR_VARIABLE_DESC, winml/WINML_TENSOR_VARIABLE_DESC
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
targetos: Windows
req.typenames: WINML_TENSOR_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINML_TENSOR_VARIABLE_DESC
 - winml/WINML_TENSOR_VARIABLE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winml.h
api_name:
 - WINML_TENSOR_VARIABLE_DESC
---

# WINML_TENSOR_VARIABLE_DESC structure


## -description

<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains description properties of the tensor variable.

## -struct-fields

### -field ElementType

A <a href="/windows/desktop/api/winml/ne-winml-winml_tensor_data_type">WINML_TENSOR_DATA_TYPE</a> containing the element tensor data type.

### -field NumDimensions

The tensor variable dimension count.

### -field pShape

The shape of the tensor variable.