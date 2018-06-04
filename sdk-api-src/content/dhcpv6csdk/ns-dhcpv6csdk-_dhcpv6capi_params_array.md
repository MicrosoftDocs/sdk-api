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

# _DHCPV6CAPI_PARAMS_ARRAY structure


## -description


The <b>DHCPV6CAPI_PARAMS_ARRAY</b> structure contains an array of requested parameters.


## -struct-fields




### -field nParams

Number of parameters in the array.


### -field Params

Pointer to a <a href="https://msdn.microsoft.com/a8978435-a16d-446d-9bd3-4a2dc6c9ec1a">DHCPV6CAPI_PARAMS</a> structure that contains a parameter.

