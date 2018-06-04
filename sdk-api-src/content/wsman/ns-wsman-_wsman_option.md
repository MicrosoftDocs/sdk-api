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

# _WSMAN_OPTION structure


## -description


Represents a specific option name and value pair.  An option that is not understood and has a <b>mustComply</b> value of <b>TRUE</b> should result in the plug-in operation failing the request with an error.


## -struct-fields




### -field name

Specifies the name of the option.


### -field value

Specifies the value of the option.


### -field mustComply

Specifies whether the option must be understood and complied with.  If this value is <b>TRUE</b>, the plug-in must understand and adhere to the meaning of the option; otherwise, the plug-in must return an error.  If this is <b>FALSE</b>, the plug-in should ignore the option if it is not understood.

