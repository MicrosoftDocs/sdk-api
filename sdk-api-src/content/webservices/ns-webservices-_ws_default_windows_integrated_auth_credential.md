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

# _WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL structure


## -description


Type for supplying a Windows Integrated Authentication credential based on the current Windows identity. If this credential subtype is used for a security binding, the current thread token on the thread that calls <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> or <a href="https://msdn.microsoft.com/b8a0afc7-2004-419d-8ab2-ce197c7e396d">WsOpenServiceProxy</a> is used as the Windows identity when sending messages or making service calls.


<a href="https://msdn.microsoft.com/e18e0005-89bd-435e-9a12-6602c3c638b7">WsAcceptChannel</a> and <a href="https://msdn.microsoft.com/4e6ef553-7f0e-4ed7-bbdd-e85d4e0a095c">WsOpenServiceHost</a> do not support this credential type when called from an impersonating thread. 


This type derives from the base type <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>. For an instance of this type, the type selector field <b>credential.credentialType</b> must have the value <b>WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL_TYPE</b>. 




## -struct-fields




### -field credential


The base type from which this type and all other Windows Integrated Authentication credential types derive.
                See <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a>.

