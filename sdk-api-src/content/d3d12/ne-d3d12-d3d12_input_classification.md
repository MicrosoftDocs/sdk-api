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

# D3D12_INPUT_CLASSIFICATION enumeration


## -description


Identifies the type of data contained in an input slot.


## -enum-fields




### -field D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA

Input data is per-vertex data.


### -field D3D12_INPUT_CLASSIFICATION_PER_INSTANCE_DATA

Input data is per-instance data.


## -remarks




          Specify one of these values in the member of a <a href="https://msdn.microsoft.com/FDE49FD5-9F7D-4A57-9AE9-F167AF39B06C">D3D12_INPUT_ELEMENT_DESC</a> structure to specify the type of data for the input element of a pipeline state object.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

