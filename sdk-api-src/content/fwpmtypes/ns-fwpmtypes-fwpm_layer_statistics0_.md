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

# FWPM_LAYER_STATISTICS0_ structure


## -description


The <b>FWPM_LAYER_STATISTICS0</b> structure stores statistics related to a layer.


## -struct-fields




### -field layerId

Type: <b>GUID</b>

Identifier of the layer.


### -field classifyPermitCount

Type: <b>UINT32</b>

Number of permitted connections.


### -field classifyBlockCount

Type: <b>UINT32</b>

Number of blocked connections.


### -field classifyVetoCount

Type: <b>UINT32</b>

Number of vetoed connections.


### -field numCacheEntries

Type: <b>UINT32</b>


## -remarks



<b>FWPM_LAYER_STATISTICS0</b> is a specific implementation of FWPM_LAYER_STATISTICS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/c3ac6871-79b1-4378-8f3c-a56e85fd2a3b">FWPM_STATISTICS0</a>
 

 

