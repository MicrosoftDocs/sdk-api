---
UID: NF:combaseapi.CoImpersonateClient
title: CoImpersonateClient function (combaseapi.h)
description: Enables the server to impersonate the client of the current call for the duration of the call.
helpviewer_keywords: ["CoImpersonateClient","CoImpersonateClient function [COM]","_com_CoImpersonateClient","com.coimpersonateclient","combaseapi/CoImpersonateClient"]
old-location: com\coimpersonateclient.htm
tech.root: com
ms.assetid: a3cbfbbc-fc6f-4d1b-8460-1e3351cd32d7
ms.date: 12/05/2018
ms.keywords: CoImpersonateClient, CoImpersonateClient function [COM], _com_CoImpersonateClient, com.coimpersonateclient, combaseapi/CoImpersonateClient
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoImpersonateClient
 - combaseapi/CoImpersonateClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoImpersonateClient
---

# CoImpersonateClient function


## -description

Enables the server to impersonate the client of the current call for the duration of the call.



## -returns

This function supports the standard return values, including S_OK.

## -remarks

This method allows the server to impersonate the client of the current call for the duration of the call. If you do not call CoRevertToSelf, COM reverts automatically for you. This function will fail unless the object is being called with RPC_C_AUTHN_LEVEL_CONNECT or higher authentication in effect (which is any authentication level except RPC_C_AUTHN_LEVEL_NONE). This function encapsulates the following sequence of common calls (error handling excluded):


``` syntax
    CoGetCallContext(IID_IServerSecurity, (void**)&pss);
    pss->ImpersonateClient();
    pss->Release();

```

<b>CoImpersonateClient</b> encapsulates the process of getting a pointer to an instance of <a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a> that contains data about the current call, calling its <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">ImpersonateClient</a> method, and then releasing the pointer. One call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself">CoRevertToSelf</a> (or <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-reverttoself">IServerSecurity::RevertToSelf</a>) will undo any number of  calls to impersonate the client.

## -see-also

<a href="/windows/desktop/com/cloaking">Cloaking</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-impersonateclient">IServerSecurity::ImpersonateClient</a>



<a href="/windows/desktop/com/impersonation">Impersonation</a>



<a href="/windows/desktop/com/impersonation-and-asynchronous-calls">Impersonation and Asynchronous Calls</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>
