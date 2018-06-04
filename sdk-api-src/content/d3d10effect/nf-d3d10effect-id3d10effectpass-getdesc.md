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

# ID3D10EffectPass::GetDesc


## -description


Get a pass description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/e48103f3-277f-4f24-9a76-e2b728bfbe75">D3D10_PASS_DESC</a>*</b>

A pointer to a pass description (see <a href="https://msdn.microsoft.com/e48103f3-277f-4f24-9a76-e2b728bfbe75">D3D10_PASS_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures). An effect technique contains one or more passes. See <a href="https://msdn.microsoft.com/674ed278-102c-43da-a6bf-58e084df151e">techniques and passes</a>.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>



<a href="https://msdn.microsoft.com/50407b6a-a05b-41e3-90a9-b0165378b177">ID3D10EffectPass</a>
 

 

