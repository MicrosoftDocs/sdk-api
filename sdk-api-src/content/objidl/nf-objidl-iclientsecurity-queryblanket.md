---
UID: NF:objidl.IClientSecurity.QueryBlanket
title: IClientSecurity::QueryBlanket (objidl.h)
description: Retrieves authentication information the client uses to make calls on the specified proxy.
helpviewer_keywords: ["IClientSecurity interface [COM]","QueryBlanket method","IClientSecurity.QueryBlanket","IClientSecurity::QueryBlanket","QueryBlanket","QueryBlanket method [COM]","QueryBlanket method [COM]","IClientSecurity interface","_com_iclientsecurity_queryblanket","com.iclientsecurity_queryblanket","objidlbase/IClientSecurity::QueryBlanket"]
old-location: com\iclientsecurity_queryblanket.htm
tech.root: com
ms.assetid: 8761bb58-9f28-4fe6-bf24-2687608ec5e8
ms.date: 12/05/2018
ms.keywords: IClientSecurity interface [COM],QueryBlanket method, IClientSecurity.QueryBlanket, IClientSecurity::QueryBlanket, QueryBlanket, QueryBlanket method [COM], QueryBlanket method [COM],IClientSecurity interface, _com_iclientsecurity_queryblanket, com.iclientsecurity_queryblanket, objidlbase/IClientSecurity::QueryBlanket
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IClientSecurity::QueryBlanket
 - objidl/IClientSecurity::QueryBlanket
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
 - IClientSecurity.QueryBlanket
---

# IClientSecurity::QueryBlanket


## -description

Retrieves authentication information the client uses to make calls on the specified proxy.

## -parameters

### -param pProxy [in]

A pointer to the proxy. This parameter cannot be <b>NULL</b>. For more information, see the Remarks section.

### -param pAuthnSvc [out]

The current authentication service. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-service-constants">authentication service constants</a>. This parameter cannot be <b>NULL</b>.

### -param pAuthzSvc [out]

The current authorization service. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authorization-constants">authorization constants</a>. This parameter cannot be <b>NULL</b>.

### -param pServerPrincName [out]

The current principal name. The string will be allocated by the callee using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function and must be freed by the caller using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. Note that the actual principal name is returned. The EOAC_MAKE_FULLSIC flag is not accepted to convert the prinicpal name. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.

### -param pAuthnLevel [out]

The current authentication level. This will be a single value taken from the list of <a href="/windows/desktop/com/com-authentication-level-constants">authentication level constants</a>. If this parameter is <b>NULL</b>, the current authentication level is not retrieved.

### -param pImpLevel [out]

The current impersonation level. This will be a single value taken from the list of <a href="/windows/desktop/com/com-impersonation-level-constants">impersonation level constants</a>. If this parameter is <b>NULL</b>, the current impersonation level is not retrieved.

### -param pAuthInfo [out]

A pointer to a handle indicating the identity of the client that was passed to the last <a href="/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket">IClientSecurity::SetBlanket</a> call (or the default value). Default values are only valid until the proxy is released. If the caller specifies <b>NULL</b>, the client identity is not retrieved. 

The format of the structure that the returned handle refers to depends on the authentication service. For NTLMSSP and Kerberos, if the client specified a structure in the <i>pAuthInfo</i> parameter to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>, that value is returned. For Schannel, if a certificate for the client could be retrieved from the certificate manager, that value is returned here. Otherwise, <b>NULL</b> is returned. Because this points to the value itself and is not a copy, it should not be manipulated or freed.

### -param pCapabilites [out]

The capabilities of the proxy. These flags are defined in the <a href="/windows/desktop/api/objidl/ne-objidl-eole_authentication_capabilities">EOLE_AUTHENTICATION_CAPABILITIES</a> enumeration. If this parameter is <b>NULL</b>, the current capability flags are not retrieved.

## -returns

This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to create the <i>pServerPrincName</i> buffer.

</td>
</tr>
</table>

## -remarks

<b>QueryBlanket</b> is called by the client to retrieve the authentication information COM will use on calls made from the specified interface proxy. With a pointer to an interface on the proxy, the client would first call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for a pointer to <a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>; then, with this pointer, the client would call <b>QueryBlanket</b>, followed by releasing the pointer. This sequence of calls is encapsulated in the helper function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>.

In <i>pProxy</i>, you pass an interface pointer. However, you cannot pass a pointer to an interface that does not use a proxy. Thus you cannot pass a pointer to an interface that has the local keyword in its interface definition since no proxy is created for such an interface. <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> is the exception to this rule.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket">CoQueryProxyBlanket</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket">CoSetProxyBlanket</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iclientsecurity">IClientSecurity</a>