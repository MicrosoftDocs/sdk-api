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

# _WSMAN_ENVIRONMENT_VARIABLE_SET structure


## -description


Defines an array of environment variables.


## -struct-fields




### -field varsCount

Specifies the number of environment variables contained within the <b>vars</b> array.


### -field vars

Defines an array of environment variables. Each element of the array is of type <a href="https://msdn.microsoft.com/0bf58de5-0c0b-4dc2-ba8b-c75e8201adc8">WSMAN_ENVIRONMENT_VARIABLE</a>.

