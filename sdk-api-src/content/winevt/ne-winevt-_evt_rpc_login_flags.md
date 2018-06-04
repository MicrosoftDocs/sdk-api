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

# _EVT_RPC_LOGIN_FLAGS enumeration


## -description


Defines the types of authentication that you can use to authenticate the user when connecting to a remote computer.


## -enum-fields




### -field EvtRpcLoginAuthDefault

Use the default authentication method during RPC login. The default authentication method is Negotiate.


### -field EvtRpcLoginAuthNegotiate

Use the Negotiate authentication method during RPC login. The client and server negotiate whether to use NTLM or Kerberos.


### -field EvtRpcLoginAuthKerberos

Use Kerberos authentication during RPC login.


### -field EvtRpcLoginAuthNTLM

  Use NTLM authentication during RPC login.


## -see-also




<a href="https://msdn.microsoft.com/8d53402b-2d2c-4f93-8e98-4449701052b0">EVT_LOGIN_CLASS</a>



<a href="https://msdn.microsoft.com/38f74619-1643-461f-b04b-c15567c06ca8">EVT_RPC_LOGIN</a>



<a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a>
 

 

