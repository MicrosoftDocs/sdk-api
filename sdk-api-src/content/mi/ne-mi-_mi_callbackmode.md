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

# _MI_CallbackMode enumeration


## -description


Defines the callback mode  for the CIM extensions for <b>WriteError</b> and <b>PromptUser</b> functions.


## -enum-fields




### -field MI_CALLBACKMODE_REPORT

Report the details to the client, but the provider will receive a preconfigured response.  The provider does not wait for the client to receive the request before continuing.


### -field MI_CALLBACKMODE_INQUIRE

Query the  client to determine whether  the provider should continue.


### -field MI_CALLBACKMODE_IGNORE



