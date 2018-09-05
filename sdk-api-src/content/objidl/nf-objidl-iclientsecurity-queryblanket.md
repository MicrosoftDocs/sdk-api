---
UID: NF:objidl.IClientSecurity.QueryBlanket
title: IClientSecurity::QueryBlanket
author: windows-sdk-content
description: Retrieves authentication information the client uses to make calls on the specified proxy.
old-location: com\iclientsecurity_queryblanket.htm
old-project: com
ms.assetid: 8761bb58-9f28-4fe6-bf24-2687608ec5e8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IClientSecurity interface [COM],QueryBlanket method, IClientSecurity.QueryBlanket, IClientSecurity::QueryBlanket, QueryBlanket, QueryBlanket method [COM], QueryBlanket method [COM],IClientSecurity interface, _com_iclientsecurity_queryblanket, com.iclientsecurity_queryblanket, objidlbase/IClientSecurity::QueryBlanket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.redist: 
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IClientSecurity.QueryBlanket
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IClientSecurity::QueryBlanket


## -description


Retrieves authentication information the client uses to make calls on the specified proxy.


## -parameters




### -param pProxy [in]

A pointer to the proxy. This parameter cannot be <b>NULL</b>. For more information, see the Remarks section.


### -param pAuthnSvc [out]

The current authentication service. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">authentication service constants</a>. This parameter cannot be <b>NULL</b>.


### -param pAuthzSvc [out]

The current authorization service. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">authorization constants</a>. This parameter cannot be <b>NULL</b>.


### -param pServerPrincName [out]

The current principal name. The string will be allocated by the callee using the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function and must be freed by the caller using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function. Note that the actual principal name is returned. The EOAC_MAKE_FULLSIC flag is not accepted to convert the prinicpal name. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.


### -param pAuthnLevel [out]

The current authentication level. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">authentication level constants</a>. If this parameter is <b>NULL</b>, the current authentication level is not retrieved.


### -param pImpLevel [out]

The current impersonation level. This will be a single value taken from the list of <a href="https://msdn.microsoft.com/ea5a3b46-b607-4192-a3cc-b2ec55ca94a6">impersonation level constants</a>. If this parameter is <b>NULL</b>, the current impersonation level is not retrieved.


### -param pAuthInfo [out]

A pointer to a handle indicating the identity of the client that was passed to the last <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> call (or the default value). Default values are only valid until the proxy is released. If the caller specifies <b>NULL</b>, the client identity is not retrieved. 

The format of the structure that the returned handle refers to depends on the authentication service. For NTLMSSP and Kerberos, if the client specified a structure in the <i>pAuthInfo</i> parameter to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>, that value is returned. For Schannel, if a certificate for the client could be retrieved from the certificate manager, that value is returned here. Otherwise, <b>NULL</b> is returned. Because this points to the value itself and is not a copy, it should not be manipulated or freed.


### -param pCapabilites [out]

The capabilities of the proxy. These flags are defined in the <a href="https://msdn.microsoft.com/cf3396d0-6674-4f12-bd4a-227a8d32bc92">EOLE_AUTHENTICATION_CAPABILITIES</a> enumeration. If this parameter is <b>NULL</b>, the current capability flags are not retrieved.


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



<b>QueryBlanket</b> is called by the client to retrieve the authentication information COM will use on calls made from the specified interface proxy. With a pointer to an interface on the proxy, the client would first call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for a pointer to <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a>; then, with this pointer, the client would call <b>QueryBlanket</b>, followed by releasing the pointer. This sequence of calls is encapsulated in the helper function <a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>.

In <i>pProxy</i>, you pass an interface pointer. However, you cannot pass a pointer to an interface that does not use a proxy. Thus you cannot pass a pointer to an interface that has the local keyword in its interface definition since no proxy is created for such an interface. <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> is the exception to this rule.




## -see-also




<a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>



<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a>
 

 

