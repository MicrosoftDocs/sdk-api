---
UID: NS:winml.WINML_VARIABLE_DESC
title: WINML_VARIABLE_DESC (winml.h)
author: windows-sdk-content
description: Contains description properties of the variable.
old-location: machinelearning\winml_variable_desc.htm
tech.root: MachineLearning
ms.assetid: 94FBC8E4-13BD-49A5-A720-0827479A43A6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MachineLearning.winml_variable_desc, PWINML_VARIABLE_DESC, PWINML_VARIABLE_DESC structure pointer, WINML_VARIABLE_DESC, WINML_VARIABLE_DESC structure, winml/PWINML_VARIABLE_DESC, winml/WINML_VARIABLE_DESC
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
 - WINML_VARIABLE_DESC
product: Windows
targetos: Windows
req.typenames: WINML_VARIABLE_DESC
req.redist: 
ms.custom: 19H1
---

# WINML_VARIABLE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Contains description properties of the variable.


## -struct-fields




### -field Name

The name of the variable.


### -field Description

The description of the variable.


### -field FeatureType

A <a href="https://msdn.microsoft.com/179DD392-15B6-4BDE-8BD3-91256951DCD3">WINML_FEATURE_TYPE</a> containing the feature type of variable.


### -field Required

<b>true</b> if the variable is required; otherwise, <b>false</b>.


### -field Tensor

A <a href="https://msdn.microsoft.com/71D65FC6-7A2B-40D6-B040-213C8BC77BE0">WINML_TENSOR_VARIABLE_DESC</a> containing the description of the tensor variable.


### -field Sequence

A <a href="https://msdn.microsoft.com/6350AFEE-8E1A-4C21-8017-9D3E9EC601F8">WINML_SEQUENCE_VARIABLE_DESC</a> containing the description of the sequence variable.


### -field Map

A <a href="https://msdn.microsoft.com/897AA848-EE56-47BF-8CCC-95B6F91D7EE5">WINML_MAP_VARIABLE_DESC</a> containing the description of the map variable.


### -field Image

A <a href="https://msdn.microsoft.com/82EE6D9B-08C4-4128-BE8A-DF922AA7318E">WINML_IMAGE_VARIABLE_DESC</a> containing the description of the image variable.

