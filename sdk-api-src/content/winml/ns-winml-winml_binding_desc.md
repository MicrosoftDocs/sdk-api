---
UID: NS:winml.WINML_BINDING_DESC
title: WINML_BINDING_DESC (winml.h)
description: Contains a description of the WinML binding.
helpviewer_keywords: ["MachineLearning.winml_binding_desc","PWINML_BINDING_DESC","PWINML_BINDING_DESC structure pointer","WINML_BINDING_DESC","WINML_BINDING_DESC structure","winml/PWINML_BINDING_DESC","winml/WINML_BINDING_DESC"]
old-location: machinelearning\winml_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 928C2AD0-73DD-4ECA-AC54-36ED84A9E4E6
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_binding_desc, PWINML_BINDING_DESC, PWINML_BINDING_DESC structure pointer, WINML_BINDING_DESC, WINML_BINDING_DESC structure, winml/PWINML_BINDING_DESC, winml/WINML_BINDING_DESC
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
req.typenames: WINML_BINDING_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINML_BINDING_DESC
 - winml/WINML_BINDING_DESC
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
 - WINML_BINDING_DESC
---

# WINML_BINDING_DESC structure


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains a description of the WinML binding.

## -struct-fields

### -field Name

The name of the WinML binding.

### -field BindType

A <a href="/windows/desktop/api/winml/ne-winml-winml_binding_type">WINML_BINDING_TYPE</a> containing the type of the WinML binding.

### -field Tensor

A <a href="/windows/desktop/api/winml/ns-winml-winml_tensor_binding_desc">WINML_TENSOR_BINDING_DESC</a> containing the description of the tensor binding.

### -field Sequence

A <a href="/windows/desktop/api/winml/ns-winml-winml_sequence_binding_desc">WINML_SEQUENCE_BINDING_DESC</a> containing the description of the sequence binding.

### -field Map

A <a href="/windows/desktop/api/winml/ns-winml-winml_map_binding_desc">WINML_MAP_BINDING_DESC</a> containing the description of the map binding.

### -field Image

A <a href="/windows/desktop/api/winml/ns-winml-winml_image_binding_desc">WINML_IMAGE_BINDING_DESC</a> containing the description of the image binding.

### -field Resource

A <a href="/windows/desktop/api/winml/ns-winml-winml_resource_binding_desc">WINML_RESOURCE_BINDING_DESC</a> containing the description of the resource binding.