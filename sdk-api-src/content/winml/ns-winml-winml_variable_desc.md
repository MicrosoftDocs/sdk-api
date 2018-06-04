---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WINML_VARIABLE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

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

