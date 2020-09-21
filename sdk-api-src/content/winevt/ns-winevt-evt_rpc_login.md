---
UID: NS:winevt._EVT_RPC_LOGIN
title: EVT_RPC_LOGIN (winevt.h)
description: Contains the information used to connect to a remote computer.
helpviewer_keywords: ["EVT_RPC_LOGIN","EVT_RPC_LOGIN structure [EventLog]","wes.evt_rpc_login","winevt/_EVT_RPC_LOGIN"]
old-location: wes\evt_rpc_login.htm
tech.root: wes
ms.assetid: 38f74619-1643-461f-b04b-c15567c06ca8
ms.date: 12/05/2018
ms.keywords: EVT_RPC_LOGIN, EVT_RPC_LOGIN structure [EventLog], wes.evt_rpc_login, winevt/_EVT_RPC_LOGIN
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
req.typenames: EVT_RPC_LOGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_RPC_LOGIN
 - winevt/_EVT_RPC_LOGIN
 - EVT_RPC_LOGIN
 - winevt/EVT_RPC_LOGIN
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
 - EVT_RPC_LOGIN
---

# EVT_RPC_LOGIN structure


## -description

Contains the information used to connect to a remote computer.

## -struct-fields

### -field Server

The name of the remote computer to connect to.

### -field User

The user name to use to connect to the remote computer.

### -field Domain

The domain to which the user account belongs. Optional.

### -field Password

The password for the user account.

### -field Flags

The authentication method to use to authenticate the user when connecting to the remote computer. For possible authentication methods, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_rpc_login_flags">EVT_RPC_LOGIN_FLAGS</a> enumeration.

## -remarks

You can set <b>User</b>, <b>Domain</b>, and <b>Password</b> to <b>NULL</b> to use the credentials of the current user.

If you set <b>Password</b>, consider using the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function to clear the password after calling <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a>.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a>