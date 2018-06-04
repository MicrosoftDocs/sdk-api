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

# _WSD_CONFIG_PARAM structure


## -description


Represents configuration parameters for creating <code>WSDAPI</code> objects.


## -struct-fields




### -field configParamType

A <a href="https://msdn.microsoft.com/46189d61-79d0-4ec9-82eb-ac1331201490">WSD_CONFIG_PARAM_TYPE</a> value that indicates the type configuration data contained in this structure.


### -field pConfigData

A pointer to a single configuration data structure.   The <i>configParamType</i> member specifies the type of data passed in.


### -field dwConfigDataSize

The size of the configuration data in <i>pConfigData</i>.

