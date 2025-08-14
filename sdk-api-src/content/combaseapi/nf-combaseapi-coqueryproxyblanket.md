---
UID: NF:combaseapi.CoQueryProxyBlanket
title: CoQueryProxyBlanket function (combaseapi.h)
description: Retrieves the authentication information the client uses to make calls on the specified proxy.
helpviewer_keywords: ["CoQueryProxyBlanket","CoQueryProxyBlanket function [COM]","_com_CoQueryProxyBlanket","com.coqueryproxyblanket","combaseapi/CoQueryProxyBlanket"]
old-location: com\coqueryproxyblanket.htm
tech.root: com
ms.assetid: e613e06a-0900-413e-bde2-39ce1612fed1
ms.date: 12/05/2018
ms.keywords: CoQueryProxyBlanket, CoQueryProxyBlanket function [COM], _com_CoQueryProxyBlanket, com.coqueryproxyblanket, combaseapi/CoQueryProxyBlanket
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
 - CoQueryProxyBlanket
 - combaseapi/CoQueryProxyBlanket
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
 - CoQueryProxyBlanket
---

# CoQueryProxyBlanket function


## -description

Retrieves the authentication information the client uses to make calls on the specified proxy. This is a helper function for <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-queryblanket">IClientSecurity::QueryBlanket</a>.

## -parameters

### -param pProxy [in]

A pointer indicating the proxy to query. This parameter cannot be <b>NULL</b>. For more information, see the Remarks section.

### -param pwAuthnSvc [out, optional]

A pointer to a variable that receives the current authentication service. This will be a single value taken from the <a href="/windows/desktop/com/com-authentication-service-constants">authentication service constants</a>. This parameter cannot be <b>NULL</b>.

### -param pAuthzSvc [out, optional]

A pointer to a variable that receives the current authorization service. This will be a single value taken from the <a href="/windows/desktop/com/com-authorization-constants">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.

### -param pServerPrincName [out, optional]

The current principal name. The string will be allocated by the callee using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. The EOAC_MAKE_FULLSIC flag is not accepted in the <i>pCapabilities</i> parameter. For more information about the msstd and fullsic forms, see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.

### -param pAuthnLevel [out, optional]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the <a href="/windows/desktop/com/com-authentication-level-constants">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.

### -param pImpLevel [out, optional]

A pointer to a variable that receives the current impersonation level. This will be a single value taken from the <a href="/windows/desktop/com/com-impersonation-level-constants">impersonation level constants</a>. If the caller specifies <b>NULL</b>, the current impersonation level is not retrieved.

### -param pAuthInfo [out, optional]

A pointer to a handle that receives the identity of the client that was passed to the last <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> call (or the default value). Default values are only valid until the proxy is released. If the caller specifies <b>NULL</b>, the client identity is not retrieved. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. For NTLMSSP and Kerberos, if the client specified a structure in the <i>pAuthInfo</i> parameter to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>, that value is returned. For Schannel, if a certificate for the client could be retrieved from the certificate manager, that value is returned here. Otherwise, <b>NULL</b> is returned. See <a href="/windows/desktop/Rpc/rpc-auth-identity-handle">RPC_AUTH_IDENTITY_HANDLE</a>.

### -param pCapabilites [out, optional]

A pointer to a variable that receives the capabilities of the proxy. If the caller specifies <b>NULL</b>, the current capability flags are not retrieved.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<b>CoQueryProxyBlanket</b> is called by the client to retrieve the authentication information COM will use on calls made from the specified proxy. This function encapsulates the following sequence of common calls (error handling excluded):




``` syntax
pProxy->QueryInterface(IID_IClientSecurity, (void**)&pcs);
pcs->QueryBlanket(
    pProxy, pAuthnSvc, pAuthzSvc, pServerPrincName, pAuthnLevel, pImpLevel, ppAuthInfo, pCapabilities
  );
pcs->Release();

```

This sequence calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the proxy to get a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>, and with the resulting pointer, calls <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-queryblanket">IClientSecurity::QueryBlanket</a> and then releases the pointer.

In <i>pProxy</i>, you can pass any proxy, such as a proxy you get through a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>, or you can pass an interface pointer. It can be any interface. You cannot pass a pointer to something that is not a proxy. Therefore, you can't pass a pointer to an interface that has the local keyword in its interface definition because no proxy is created for such an interface. <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> is the exception to this rule.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket">CoQueryClientBlanket</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-queryblanket">IClientSecurity::QueryBlanket</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>
