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

# TF_SELECTION structure


## -description



The <b>TF_SELECTION</b> structure contains text selection data.




## -struct-fields




### -field range

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that specifies the selected text.


### -field style

A <a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">TF_SELECTIONSTYLE</a> structure that contains selection data.


## -see-also




<a href="https://msdn.microsoft.com/08b67fd5-aebe-49f7-af78-6f49c8f47f64">ITfContext::GetSelection
      </a>



<a href="https://msdn.microsoft.com/1cf50b5e-6ec2-4649-9acc-743a2e3d8096">
        ITfContext::SetSelection
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>



<a href="https://msdn.microsoft.com/3a38172b-611b-445f-be24-ea2a19178255">
        TF_SELECTIONSTYLE
      </a>
 

 

