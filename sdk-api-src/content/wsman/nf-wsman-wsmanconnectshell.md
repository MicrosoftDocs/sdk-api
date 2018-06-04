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

# WSManConnectShell function


## -description


Connects to an existing server session.


## -parameters




### -param session [in, out]

Specifies the session handle returned by a <a href="https://msdn.microsoft.com/5123d876-5123-4fa4-8f6f-859a26aad825">WSManCreateSession</a> function. This parameter cannot be NULL.


### -param flags

Reserved for future use. Must be zero.


### -param resourceUri [in]

Defines the shell type  to which the connection will be made. The shell type is defined by a unique URI, therefore the shell object returned by the call is dependent on the URI that is specified by this parameter. The <i>resourceUri</i> parameter cannot be NULL and it is a null-terminated string.


### -param shellID [in]

Specifies the shell identifier that is associated with the server shell session to which the client intends to connect.


### -param options [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a> structure that specifies a set of options for the shell. This parameter is optional.


### -param connectXml [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that defines an open context for the connect shell operation. The content should be a valid XML string. This parameter can be NULL.


### -param async [in]

Defines an asynchronous structure that contains an optional user context and a mandatory callback function. See the <a href="https://msdn.microsoft.com/9391e1a8-7048-49b8-9dc4-1da25b190238">WSMAN_SHELL_ASYNC</a> structure for more information. This parameter cannot be NULL.


### -param shell [out]

Specifies a shell handle that uniquely identifies the shell object that was returned by <i>resourceURI</i>. The resource handle tracks the client endpoint for the shell and is used by other WinRM methods to interact with the shell object. The shell object should be deleted by calling the <a href="https://msdn.microsoft.com/1da452ef-5842-4d8d-941b-09fa57393ebb">WSManCloseShell</a> method. This parameter cannot be NULL.


## -returns



This function does not return a value.




## -remarks



Connects to an existing server shell session identified by the <i>ShellId</i> parameter. This builds the necessary client side context, represented by the return parameter shell, that can be used to carry out subsequent operations such as running commands and sending and receiving output on the server shell session. 
This <b>WSManConnectShell</b> function does not automatically construct the client side contexts for any commands that are currently associated with the server shell session.



