---
UID: NF:objidlbase.IServerSecurity.QueryBlanket
title: IServerSecurity::QueryBlanket (objidlbase.h)
description: The IServerSecurity::QueryBlanket (objidlbase.h) method retrieves information about the client that invoked one of the server's methods.
helpviewer_keywords: ["IServerSecurity interface [COM]","QueryBlanket method","IServerSecurity.QueryBlanket","IServerSecurity::QueryBlanket","QueryBlanket","QueryBlanket method [COM]","QueryBlanket method [COM]","IServerSecurity interface","_com_iserversecurity_queryblanket","com.iserversecurity_queryblanket","objidlbase/IServerSecurity::QueryBlanket"]
old-location: com\iserversecurity_queryblanket.htm
tech.root: com
ms.assetid: 1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868
ms.date: 08/15/2022
ms.keywords: IServerSecurity interface [COM],QueryBlanket method, IServerSecurity.QueryBlanket, IServerSecurity::QueryBlanket, QueryBlanket, QueryBlanket method [COM], QueryBlanket method [COM],IServerSecurity interface, _com_iserversecurity_queryblanket, com.iserversecurity_queryblanket, objidlbase/IServerSecurity::QueryBlanket
req.header: objidlbase.h
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
 - IServerSecurity::QueryBlanket
 - objidlbase/IServerSecurity::QueryBlanket
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
 - IServerSecurity.QueryBlanket
---

# IServerSecurity::QueryBlanket


## -description

Retrieves information about the client that invoked one of the server's methods.

## -parameters

### -param pAuthnSvc [out]

A pointer to the current authentication service. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-service-constants">authentication service constants</a>. If the caller specifies <b>NULL</b>, the current authentication service is not retrieved.

### -param pAuthzSvc [out]

A pointer to a variable that receives the current authorization service. This will be a single value from the list of <a href="/windows/desktop/com/com-authorization-constants">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.

### -param pServerPrincName [out]

The current principal name. The string will be allocated by the callee using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. By default, Schannel principal names will be in the msstd form. The fullsic form will be returned if EOAC_MAKE_FULLSIC is specified in the <i>pCapabilities</i> parameter. For more information on the msstd and fullsic forms, see <a href="/windows/desktop/Rpc/principal-names">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.

### -param pAuthnLevel [out]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-level-constants">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.

### -param pImpLevel [out]

This parameter must be <b>NULL</b>.

### -param pPrivs [out]

The privilege information for the client application. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. The information is only valid for the duration of the current call. For NTLMSSP, and Kerberos, this is a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_auth_identity_a">SEC_WINNT_AUTH_IDENTITY</a> or <a href="/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2">SEC_WINNT_AUTH_IDENTITY_EX</a> structure. For Schannel, this is a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the client's certificate. If the client has no certificate, <b>NULL</b> is returned. If the caller specifies <b>NULL</b>, the current privilege information is not retrieved.

### -param pCapabilities [in, out]

The capabilities of the call. To request that the principal name be returned in fullsic form if Schannel is the authentication service, the caller can set the EOAC_MAKE_FULLSIC flag in this parameter. If the caller specifies <b>NULL</b>, the current capabilities are not retrieved.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<b>QueryBlanket</b> is used by the server to find out about the client that invoked one of its methods. To get a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a> for the current call on the current thread, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>, specifying IID_IServerSecurity. This interface pointer may only be used in the same apartment as the call for the duration of the call.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket">CoQueryClientBlanket</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iserversecurity">IServerSecurity</a>
