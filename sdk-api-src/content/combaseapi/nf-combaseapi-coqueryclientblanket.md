---
UID: NF:combaseapi.CoQueryClientBlanket
title: CoQueryClientBlanket function (combaseapi.h)
description: Called by the server to find out about the client that invoked the method executing on the current thread.
helpviewer_keywords: ["CoQueryClientBlanket","CoQueryClientBlanket function [COM]","_com_CoQueryClientBlanket","com.coqueryclientblanket","combaseapi/CoQueryClientBlanket"]
old-location: com\coqueryclientblanket.htm
tech.root: com
ms.assetid: 58a2c121-c324-4c33-aaca-490b5a09738c
ms.date: 12/05/2018
ms.keywords: CoQueryClientBlanket, CoQueryClientBlanket function [COM], _com_CoQueryClientBlanket, com.coqueryclientblanket, combaseapi/CoQueryClientBlanket
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
 - CoQueryClientBlanket
 - combaseapi/CoQueryClientBlanket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoQueryClientBlanket
---

# CoQueryClientBlanket function


## -description

Called by the server to find out about the client that invoked the method executing on the current thread. This is a helper function for <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-queryblanket">IServerSecurity::QueryBlanket</a>.

## -parameters

### -param pAuthnSvc [out, optional]

A pointer to a variable that receives the current authentication service. This will be a single value taken from the <a href="/windows/desktop/com/com-authentication-service-constants">authentication service constants</a>. If the caller specifies <b>NULL</b>, the current authentication service is not retrieved.

### -param pAuthzSvc [out, optional]

A pointer to a variable that receives the current authorization service. This will be a single value taken from the <a href="/windows/desktop/com/com-authorization-constants">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.

### -param pServerPrincName [out, optional]

The current principal name. The string will be allocated by the callee using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. By default, Schannel principal names will be in the msstd form. The fullsic form will be returned if EOAC_MAKE_FULLSIC is specified in the <i>pCapabilities</i> parameter. For more information about the msstd and fullsic forms, see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.

### -param pAuthnLevel [out, optional]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the <a href="/windows/desktop/com/com-authentication-level-constants">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.

### -param pImpLevel [out, optional]

This parameter must be <b>NULL</b>.

### -param pPrivs [out, optional]

A pointer to a handle that receives the privilege information for the client application. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. The information is valid only for the duration of the current call. For NTLMSSP and Kerberos, this is a string identifying the client principal. For Schannel, this is a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the client's certificate. If the client has no certificate, <b>NULL</b> is returned. If the caller specifies <b>NULL</b>, the current privilege information is not retrieved. See <a href="/windows/desktop/Rpc/rpc-authz-handle">RPC_AUTHZ_HANDLE</a>.

### -param pCapabilities [in, out, optional]

A pointer to return flags indicating capabilities of the call. To request that the principal name be returned in fullsic form if Schannel is the authentication service, the caller can set the EOAC_MAKE_FULLSIC flag in this parameter. If the caller specifies <b>NULL</b>, the current capabilities are not retrieved.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<b>CoQueryClientBlanket</b> is called by the server to get security information about the client that invoked the method executing on the current thread. This function encapsulates the following sequence of common calls (error handling excluded):




``` syntax
    CoGetCallContext(IID_IServerSecurity, (void**)&pss);
    pss->QueryBlanket(pAuthnSvc, pAuthzSvc, pServerPrincName, 
                pAuthnLevel, pImpLevel, pPrivs, pCapabilities);
    pss->Release();

```

This sequence calls <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a> to get a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a> and, with the resulting pointer, calls <a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-queryblanket">IServerSecurity::QueryBlanket</a> and then releases the pointer.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iserversecurity-queryblanket">IServerSecurity::QueryBlanket</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>
