---
UID: NF:combaseapi.CoQueryProxyBlanket
title: CoQueryProxyBlanket function
author: windows-sdk-content
description: Retrieves the authentication information the client uses to make calls on the specified proxy.
old-location: com\coqueryproxyblanket.htm
tech.root: com
ms.assetid: e613e06a-0900-413e-bde2-39ce1612fed1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CoQueryProxyBlanket, CoQueryProxyBlanket function [COM], _com_CoQueryProxyBlanket, com.coqueryproxyblanket, combaseapi/CoQueryProxyBlanket
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoQueryProxyBlanket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoQueryProxyBlanket function


## -description


Retrieves the authentication information the client uses to make calls on the specified proxy. This is a helper function for <a href="https://msdn.microsoft.com/8761bb58-9f28-4fe6-bf24-2687608ec5e8">IClientSecurity::QueryBlanket</a>.



## -parameters




### -param pProxy [in]

A pointer indicating the proxy to query. This parameter cannot be <b>NULL</b>. For more information, see the Remarks section.


### -param pwAuthnSvc [out, optional]

A pointer to a variable that receives the current authentication service. This will be a single value taken from the <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">authentication service constants</a>. This parameter cannot be <b>NULL</b>.


### -param pAuthzSvc [out, optional]

A pointer to a variable that receives the current authorization service. This will be a single value taken from the <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.


### -param pServerPrincName [out, optional]

The current principal name. The string will be allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. The EOAC_MAKE_FULLSIC flag is not accepted in the <i>pCapabilities</i> parameter. For more information about the msstd and fullsic forms, see <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.


### -param pAuthnLevel [out, optional]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.


### -param pImpLevel [out, optional]

A pointer to a variable that receives the current impersonation level. This will be a single value taken from the <a href="https://msdn.microsoft.com/ea5a3b46-b607-4192-a3cc-b2ec55ca94a6">impersonation level constants</a>. If the caller specifies <b>NULL</b>, the current impersonation level is not retrieved.


### -param pAuthInfo [out, optional]

A pointer to a handle that receives the identity of the client that was passed to the last <a href="https://msdn.microsoft.com/adb35089-2846-4782-8c96-d3d1e14beed9">IClientSecurity::SetBlanket</a> call (or the default value). Default values are only valid until the proxy is released. If the caller specifies <b>NULL</b>, the client identity is not retrieved. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. For NTLMSSP and Kerberos, if the client specified a structure in the <i>pAuthInfo</i> parameter to <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>, that value is returned. For Schannel, if a certificate for the client could be retrieved from the certificate manager, that value is returned here. Otherwise, <b>NULL</b> is returned. See <a href="https://msdn.microsoft.com/06e45348-a392-45be-9f8a-e77ef887f26c">RPC_AUTH_IDENTITY_HANDLE</a>.


### -param pCapabilites [out, optional]

A pointer to a variable that receives the capabilities of the proxy. If the caller specifies <b>NULL</b>, the current capability flags are not retrieved.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<b>CoQueryProxyBlanket</b> is called by the client to retrieve the authentication information COM will use on calls made from the specified proxy. This function encapsulates the following sequence of common calls (error handling excluded):



<pre class="syntax" xml:space="preserve"><code>pProxy-&gt;QueryInterface(IID_IClientSecurity, (void**)&amp;pcs);
pcs-&gt;QueryBlanket(
    pProxy, pAuthnSvc, pAuthzSvc, pServerPrincName, pAuthnLevel, pImpLevel, ppAuthInfo, pCapabilities
  );
pcs-&gt;Release();
</code></pre>
This sequence calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the proxy to get a pointer to <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a>, and with the resulting pointer, calls <a href="https://msdn.microsoft.com/8761bb58-9f28-4fe6-bf24-2687608ec5e8">IClientSecurity::QueryBlanket</a> and then releases the pointer.

In <i>pProxy</i>, you can pass any proxy, such as a proxy you get through a call to <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> or <a href="https://msdn.microsoft.com/d0eac0da-2f41-40c4-b756-31bc22752c17">CoUnmarshalInterface</a>, or you can pass an interface pointer. It can be any interface. You cannot pass a pointer to something that is not a proxy. Therefore, you can't pass a pointer to an interface that has the local keyword in its interface definition because no proxy is created for such an interface. <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> is the exception to this rule.





## -see-also




<a href="https://msdn.microsoft.com/58a2c121-c324-4c33-aaca-490b5a09738c">CoQueryClientBlanket</a>



<a href="https://msdn.microsoft.com/c2e5e681-8fa5-4b02-b59d-ba796eb0dccf">CoSetProxyBlanket</a>



<a href="https://msdn.microsoft.com/8761bb58-9f28-4fe6-bf24-2687608ec5e8">IClientSecurity::QueryBlanket</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

