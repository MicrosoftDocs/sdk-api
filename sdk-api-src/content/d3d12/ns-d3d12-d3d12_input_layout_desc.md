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

# D3D12_INPUT_LAYOUT_DESC structure


## -description


Describes the input-buffer data for the input-assembler stage.


## -struct-fields




### -field pInputElementDescs


            An array of <a href="https://msdn.microsoft.com/FDE49FD5-9F7D-4A57-9AE9-F167AF39B06C">D3D12_INPUT_ELEMENT_DESC</a> structures that describe the data types of the input-assembler stage.
          


### -field NumElements


            The number of input-data types in the array of input elements that the <b>pInputElementDescs</b> member points to.
          


## -remarks




        This structure is a member of the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

