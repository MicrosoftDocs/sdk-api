---
UID: NS:winml.WINML_VARIABLE_DESC
title: WINML_VARIABLE_DESC (winml.h)
description: Contains description properties of the variable.
helpviewer_keywords: ["MachineLearning.winml_variable_desc","PWINML_VARIABLE_DESC","PWINML_VARIABLE_DESC structure pointer","WINML_VARIABLE_DESC","WINML_VARIABLE_DESC structure","winml/PWINML_VARIABLE_DESC","winml/WINML_VARIABLE_DESC"]
old-location: machinelearning\winml_variable_desc.htm
tech.root: MachineLearning
ms.assetid: 94FBC8E4-13BD-49A5-A720-0827479A43A6
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_variable_desc, PWINML_VARIABLE_DESC, PWINML_VARIABLE_DESC structure pointer, WINML_VARIABLE_DESC, WINML_VARIABLE_DESC structure, winml/PWINML_VARIABLE_DESC, winml/WINML_VARIABLE_DESC
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
req.typenames: WINML_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINML_VARIABLE_DESC
 - winml/WINML_VARIABLE_DESC
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
 - WINML_VARIABLE_DESC
---

# WINML_VARIABLE_DESC structure


## -description



<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains description properties of the variable.

## -struct-fields

### -field Name

The name of the variable.

### -field Description

The description of the variable.

### -field FeatureType

A <a href="/windows/desktop/api/winml/ne-winml-winml_feature_type">WINML_FEATURE_TYPE</a> containing the feature type of variable.

### -field Required

<b>true</b> if the variable is required; otherwise, <b>false</b>.

### -field Tensor

A <a href="/windows/desktop/api/winml/ns-winml-winml_tensor_variable_desc">WINML_TENSOR_VARIABLE_DESC</a> containing the description of the tensor variable.

### -field Sequence

A <a href="/windows/desktop/api/winml/ns-winml-winml_sequence_variable_desc">WINML_SEQUENCE_VARIABLE_DESC</a> containing the description of the sequence variable.

### -field Map

A <a href="/windows/desktop/api/winml/ns-winml-winml_map_variable_desc">WINML_MAP_VARIABLE_DESC</a> containing the description of the map variable.

### -field Image

A <a href="/windows/desktop/api/winml/ns-winml-winml_image_variable_desc">WINML_IMAGE_VARIABLE_DESC</a> containing the description of the image variable.