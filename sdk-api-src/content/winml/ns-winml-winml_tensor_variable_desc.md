---
UID: NS:winml.WINML_TENSOR_VARIABLE_DESC
title: WINML_TENSOR_VARIABLE_DESC
author: windows-sdk-content
description: Contains description properties of the tensor variable.
old-location: machinelearning\winml_tensor_variable_desc.htm
old-project: MachineLearning
ms.assetid: 71D65FC6-7A2B-40D6-B040-213C8BC77BE0
ms.author: windowssdkdev
ms.date: 03/08/2018
ms.keywords: MachineLearning.winml_tensor_variable_desc, PWINML_TENSOR_VARIABLE_DESC, PWINML_TENSOR_VARIABLE_DESC structure pointer, WINML_TENSOR_VARIABLE_DESC, WINML_TENSOR_VARIABLE_DESC structure, winml/PWINML_TENSOR_VARIABLE_DESC, winml/WINML_TENSOR_VARIABLE_DESC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WINML_TENSOR_VARIABLE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winml.h
api_name:
 - WINML_TENSOR_VARIABLE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WINML_TENSOR_VARIABLE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains description properties of the tensor variable.


## -struct-fields




### -field ElementType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the element tensor data type.


### -field NumDimensions

The tensor variable dimension count.


### -field pShape

The shape of the tensor variable.

