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

# ID3D10Device::CreateBlendState


## -description


Create a blend-state object that encapsules blend state for the output-merger stage.


## -parameters




### -param pBlendStateDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">D3D10_BLEND_DESC</a>*</b>

Pointer to a blend-state description (see <a href="https://msdn.microsoft.com/c256dd1e-2b25-4dc5-8e49-5bf2b419b3c5">D3D10_BLEND_DESC</a>).


### -param ppBlendState [out]

Type: <b><a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState</a>**</b>

Address of a pointer to the blend-state object created (see <a href="https://msdn.microsoft.com/fe0186f5-cd8f-478d-9009-a0f82830cd1f">ID3D10BlendState Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An application can create up to 4096 unique blend-state objects. For each object created, the runtime checks to see if a previous object has the same state. If such a previous object exists, the runtime will return a pointer to previous instance instead of creating a duplicate object.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

