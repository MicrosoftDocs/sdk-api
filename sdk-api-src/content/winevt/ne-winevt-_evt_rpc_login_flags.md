---
UID: NE:winevt._EVT_RPC_LOGIN_FLAGS
title: "_EVT_RPC_LOGIN_FLAGS"
author: windows-sdk-content
description: Defines the types of authentication that you can use to authenticate the user when connecting to a remote computer.
old-location: wes\evt_rpc_login_flags.htm
old-project: wes
ms.assetid: f3001756-7c2d-4a96-bbdf-e707debb5374
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EVT_RPC_LOGIN_FLAGS, EVT_RPC_LOGIN_FLAGS enumeration [EventLog], EvtRpcLoginAuthDefault, EvtRpcLoginAuthKerberos, EvtRpcLoginAuthNTLM, EvtRpcLoginAuthNegotiate, _EVT_RPC_LOGIN_FLAGS, wes.evt_rpc_login_flags, winevt/EVT_RPC_LOGIN_FLAGS, winevt/EvtRpcLoginAuthDefault, winevt/EvtRpcLoginAuthKerberos, winevt/EvtRpcLoginAuthNTLM, winevt/EvtRpcLoginAuthNegotiate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EVT_RPC_LOGIN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_RPC_LOGIN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

