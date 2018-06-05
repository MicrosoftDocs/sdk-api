---
UID: NS:winml.WINML_TENSOR_BINDING_DESC
title: WINML_TENSOR_BINDING_DESC
author: windows-sdk-content
description: Contains description properties of the tensor binding.
old-location: machinelearning\winml_tensor_binding_desc.htm
old-project: MachineLearning
ms.assetid: A99A57DB-4602-4841-85FF-BC655CAB6C6F
ms.author: windowssdkdev
ms.date: 03/07/2018
ms.keywords: MachineLearning.winml_tensor_binding_desc, PWINML_TENSOR_BINDING_DESC, PWINML_TENSOR_BINDING_DESC structure pointer, WINML_TENSOR_BINDING_DESC, WINML_TENSOR_BINDING_DESC structure, winml/PWINML_TENSOR_BINDING_DESC, winml/WINML_TENSOR_BINDING_DESC
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
req.typenames: WINML_TENSOR_BINDING_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winml.h
api_name:
-	WINML_TENSOR_BINDING_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WINML_TENSOR_BINDING_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains description properties of the tensor binding.


## -struct-fields




### -field DataType

A <a href="https://msdn.microsoft.com/A8EB60A1-F769-460F-8C94-5D1DE3A1820F">WINML_TENSOR_DATA_TYPE</a> containing the WinML tensor data type.


### -field NumDimensions

The WinML tensor dimension count.


### -field pShape

A pointer to the shape of the WinML tensor.


### -field DataSize

The size of tensor data in bytes.


### -field pData

Pointer to the tensor data.

