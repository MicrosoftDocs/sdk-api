---
UID: NF:objidl.IServerSecurity.ImpersonateClient
title: IServerSecurity::ImpersonateClient (objidl.h)
description: The IServerSecurity::ImpersonateClient method (objidl.h) enables a server to impersonate a client for the duration of a call.
helpviewer_keywords: ["IServerSecurity interface [COM]","ImpersonateClient method","IServerSecurity.ImpersonateClient","IServerSecurity::ImpersonateClient","ImpersonateClient","ImpersonateClient method [COM]","ImpersonateClient method [COM]","IServerSecurity interface","_com_iserversecurity_impersonateclient","com.iserversecurity_impersonateclient","objidlbase/IServerSecurity::ImpersonateClient"]
old-location: com\iserversecurity_impersonateclient.htm
tech.root: com
ms.assetid: 20398b63-0fcb-40ab-93ed-f4c75760eb9e
ms.date: 08/15/2022
ms.keywords: IServerSecurity interface [COM],ImpersonateClient method, IServerSecurity.ImpersonateClient, IServerSecurity::ImpersonateClient, ImpersonateClient, ImpersonateClient method [COM], ImpersonateClient method [COM],IServerSecurity interface, _com_iserversecurity_impersonateclient, com.iserversecurity_impersonateclient, objidlbase/IServerSecurity::ImpersonateClient
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServerSecurity::ImpersonateClient
 - objidl/IServerSecurity::ImpersonateClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IServerSecurity.ImpersonateClient
---

# IServerSecurity::ImpersonateClient


## -description

Enables a server to impersonate a client for the duration of a call.



## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

Usually, a method executes on a thread that uses the access token of the process. However, when impersonating a client, the server runs in the client's security context so that the server has access to the resources that the client has access to. When impersonation is necessary, the server calls the <b>ImpersonateClient</b> method to cause an access token representing the client's credentials to be assigned to the current thread. This thread token is used for access checks. <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">RevertToSelf</a> restores the current thread's access token.

What the server can do on behalf of the client depends on the impersonation level set by the client, which is specified using one of the <a href="/windows/desktop/com/com-impersonation-level-constants">impersonation level constants</a>. The server may impersonate the client on an encrypted call at identify, impersonate, or delegate level. For information about these levels of impersonation, see <a href="/windows/desktop/com/impersonation-levels">Impersonation Levels</a>.

The identity presented to a server called during impersonation depends on the type of cloaking value, if any, that is set by the client. For more information, see <a href="/windows/desktop/com/cloaking">Cloaking</a>.

At the end of each method call, COM will call <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">RevertToSelf</a> if the application does not.

Traditionally, impersonation information is not nested: The last call to any impersonation mechanism overrides any previous impersonation. However, in the apartment model, impersonation is maintained during nested calls. Thus if the server A receives a call from B, impersonates, calls C, receives a call from D, impersonates, reverts, and receives the reply from C, the impersonation token will be set back to B, not A.

For information on using impersonation with asynchronous calls, see <a href="/windows/desktop/com/impersonation-and-asynchronous-calls">Impersonation and Asynchronous Calls</a>.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient">CoImpersonateClient</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a>
