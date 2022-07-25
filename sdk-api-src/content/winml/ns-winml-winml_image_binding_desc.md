---
UID: NS:winml.WINML_IMAGE_BINDING_DESC
title: WINML_IMAGE_BINDING_DESC (winml.h)
description: Contains properties for the binding of the type image.
helpviewer_keywords: ["MachineLearning.winml_image_binding_desc","PWINML_IMAGE_BINDING_DESC","PWINML_IMAGE_BINDING_DESC structure pointer","WINML_IMAGE_BINDING_DESC","WINML_IMAGE_BINDING_DESC structure","winml/PWINML_IMAGE_BINDING_DESC","winml/WINML_IMAGE_BINDING_DESC"]
old-location: machinelearning\winml_image_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 5FF6233A-8DB0-4868-925C-833B01CB9DE3
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_image_binding_desc, PWINML_IMAGE_BINDING_DESC, PWINML_IMAGE_BINDING_DESC structure pointer, WINML_IMAGE_BINDING_DESC, WINML_IMAGE_BINDING_DESC structure, winml/PWINML_IMAGE_BINDING_DESC, winml/WINML_IMAGE_BINDING_DESC
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
req.typenames: WINML_IMAGE_BINDING_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINML_IMAGE_BINDING_DESC
 - winml/WINML_IMAGE_BINDING_DESC
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
 - WINML_IMAGE_BINDING_DESC
---

# WINML_IMAGE_BINDING_DESC structure


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains properties for the binding of the type image.

## -struct-fields

### -field ElementType

A <a href="/windows/desktop/api/winml/ne-winml-winml_tensor_data_type">WINML_TENSOR_DATA_TYPE</a> describing the element tensor data type.

### -field NumDimensions

The image tensor dimension count.

### -field pShape

Pointer to the shape of the image.

### -field DataSize

Size of image data in bytes.

### -field pData

Pointer to the image data.