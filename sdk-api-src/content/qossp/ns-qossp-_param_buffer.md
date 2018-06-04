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

# _PARAM_BUFFER structure


## -description


The <b>PARAM_BUFFER</b> structure describes the format of the parameter buffer that can be included in the <a href="https://msdn.microsoft.com/604d7be8-955b-40a3-9cb4-6cbfbeeaa105">CONTROL_SERVICE</a> structure.


## -struct-fields




### -field ParameterId

Parameter ID, as defined by INTSERV.


### -field Length

Length of the entire <b>PARAM_BUFFER</b> structure.


### -field Buffer

Buffer containing the parameter.


## -see-also




<a href="https://msdn.microsoft.com/604d7be8-955b-40a3-9cb4-6cbfbeeaa105">CONTROL_SERVICE</a>
 

 

