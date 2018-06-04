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

# WSManInitialize function


## -description


Initializes the Windows Remote Management Client API. <b>WSManInitialize</b> can be used by different clients on the same process.


## -parameters




### -param flags

A flag of type <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_0</b> or <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b>.
The client that will use the disconnect-reconnect functionality should use the 
<b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> flag.


### -param apiHandle [out]

Defines a handle that uniquely identifies the client. This parameter cannot be <b>NULL</b>. When you have finished used the handle, close it by calling the <a href="https://msdn.microsoft.com/1b20ead1-cda0-4449-a454-1e695fe71de6">WSManDeinitialize</a> method.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.



