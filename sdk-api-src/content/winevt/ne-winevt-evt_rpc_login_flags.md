---
UID: NE:winevt._EVT_RPC_LOGIN_FLAGS
title: EVT_RPC_LOGIN_FLAGS (winevt.h)
description: Defines the types of authentication that you can use to authenticate the user when connecting to a remote computer.
helpviewer_keywords: ["EVT_RPC_LOGIN_FLAGS","EVT_RPC_LOGIN_FLAGS enumeration [EventLog]","EvtRpcLoginAuthDefault","EvtRpcLoginAuthKerberos","EvtRpcLoginAuthNTLM","EvtRpcLoginAuthNegotiate","wes.evt_rpc_login_flags","winevt/EVT_RPC_LOGIN_FLAGS","winevt/EvtRpcLoginAuthDefault","winevt/EvtRpcLoginAuthKerberos","winevt/EvtRpcLoginAuthNTLM","winevt/EvtRpcLoginAuthNegotiate"]
old-location: wes\evt_rpc_login_flags.htm
tech.root: wes
ms.assetid: f3001756-7c2d-4a96-bbdf-e707debb5374
ms.date: 12/05/2018
ms.keywords: EVT_RPC_LOGIN_FLAGS, EVT_RPC_LOGIN_FLAGS enumeration [EventLog], EvtRpcLoginAuthDefault, EvtRpcLoginAuthKerberos, EvtRpcLoginAuthNTLM, EvtRpcLoginAuthNegotiate, wes.evt_rpc_login_flags, winevt/EVT_RPC_LOGIN_FLAGS, winevt/EvtRpcLoginAuthDefault, winevt/EvtRpcLoginAuthKerberos, winevt/EvtRpcLoginAuthNTLM, winevt/EvtRpcLoginAuthNegotiate
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVT_RPC_LOGIN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_RPC_LOGIN_FLAGS
 - winevt/_EVT_RPC_LOGIN_FLAGS
 - EVT_RPC_LOGIN_FLAGS
 - winevt/EVT_RPC_LOGIN_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_RPC_LOGIN_FLAGS
---

# EVT_RPC_LOGIN_FLAGS enumeration


## -description

Defines the types of authentication that you can use to authenticate the user when connecting to a remote computer.

## -enum-fields

### -field EvtRpcLoginAuthDefault:0

Use the default authentication method during RPC login. The default authentication method is Negotiate.

### -field EvtRpcLoginAuthNegotiate

Use the Negotiate authentication method during RPC login. The client and server negotiate whether to use NTLM or Kerberos.

### -field EvtRpcLoginAuthKerberos

Use Kerberos authentication during RPC login.

### -field EvtRpcLoginAuthNTLM

  Use NTLM authentication during RPC login.

## -see-also

<a href="/windows/desktop/api/winevt/ne-winevt-evt_login_class">EVT_LOGIN_CLASS</a>



<a href="/windows/desktop/api/winevt/ns-winevt-evt_rpc_login">EVT_RPC_LOGIN</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a>
