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

# _WS_USERNAME_CREDENTIAL structure


## -description



The abstract base type for all username/password credentials.
            


Note that <b>WS_USERNAME_CREDENTIAL</b> and its concrete subtypes
are used with the WS-Security <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.  
They are best suitable for application-level username/password pairs, such as 
those used for online customer accounts.  The usernames and passwords specified 
are not interpreted by the security runtime, and are merely carried
client-to-server for authentication by the specified server-side
username/password validator specified by the application.
            


In contrast, the <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> and
its concrete subtypes are used for Windows Integrated Authentication
and the security bindings that use it.
            


## -struct-fields




### -field credentialType


The selector for the type of the username credential.
                

