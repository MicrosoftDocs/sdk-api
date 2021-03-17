---
UID: NS:winml.WINML_MAP_BINDING_DESC
title: WINML_MAP_BINDING_DESC (winml.h)
description: Contains properties for the binding of type map.
helpviewer_keywords: ["MachineLearning.winml_map_binding_desc","PWINML_MAP_BINDING_DESC","PWINML_MAP_BINDING_DESC structure pointer","WINML_MAP_BINDING_DESC","WINML_MAP_BINDING_DESC structure","winml/PWINML_MAP_BINDING_DESC","winml/WINML_MAP_BINDING_DESC"]
old-location: machinelearning\winml_map_binding_desc.htm
tech.root: MachineLearning
ms.assetid: 3D9FE11A-6053-4F59-9488-08A92EB45A09
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_map_binding_desc, PWINML_MAP_BINDING_DESC, PWINML_MAP_BINDING_DESC structure pointer, WINML_MAP_BINDING_DESC, WINML_MAP_BINDING_DESC structure, winml/PWINML_MAP_BINDING_DESC, winml/WINML_MAP_BINDING_DESC
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
req.typenames: WINML_MAP_BINDING_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINML_MAP_BINDING_DESC
 - winml/WINML_MAP_BINDING_DESC
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
 - WINML_MAP_BINDING_DESC
---

# WINML_MAP_BINDING_DESC structure


## -description

<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains properties for the binding of type map.

## -struct-fields

### -field ElementCount

Element count in the map binding.

### -field KeyType

A <a href="/windows/desktop/api/winml/ne-winml-winml_tensor_data_type">WINML_TENSOR_DATA_TYPE</a> containing the key element tensor data type.

### -field pStringKeys

A pointer to the key data of type string.

### -field pIntKeys

A pointer to the key data of type int.

### -field Fields

A <a href="/windows/desktop/api/winml/ne-winml-winml_tensor_data_type">WINML_TENSOR_DATA_TYPE</a> containing the field element tensor data type.

### -field pStringFields

A pointer to the field data of type string.

### -field pIntFields

A pointer to the field data of type int.

### -field pFloatFields

A Pointer to the field data of type string.

### -field pDoubleFields

A pointer to the field data of type int.