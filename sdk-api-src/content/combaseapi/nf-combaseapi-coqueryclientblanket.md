---
UID: NF:combaseapi.CoQueryClientBlanket
title: CoQueryClientBlanket function
author: windows-sdk-content
description: Called by the server to find out about the client that invoked the method executing on the current thread.
old-location: com\coqueryclientblanket.htm
tech.root: com
ms.assetid: 58a2c121-c324-4c33-aaca-490b5a09738c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CoQueryClientBlanket, CoQueryClientBlanket function [COM], _com_CoQueryClientBlanket, com.coqueryclientblanket, combaseapi/CoQueryClientBlanket
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
 - CoQueryClientBlanket
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoQueryClientBlanket function


## -description


Called by the server to find out about the client that invoked the method executing on the current thread. This is a helper function for <a href="https://msdn.microsoft.com/1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868">IServerSecurity::QueryBlanket</a>.



## -parameters




### -param pAuthnSvc [out, optional]

A pointer to a variable that receives the current authentication service. This will be a single value taken from the <a href="https://msdn.microsoft.com/c16a8e52-a7f9-40d9-99ef-10b382b5cb3c">authentication service constants</a>. If the caller specifies <b>NULL</b>, the current authentication service is not retrieved.


### -param pAuthzSvc [out, optional]

A pointer to a variable that receives the current authorization service. This will be a single value taken from the <a href="https://msdn.microsoft.com/a0bc9337-b7e4-41c5-ae36-4843fa7d98ce">authorization constants</a>. If the caller specifies <b>NULL</b>, the current authorization service is not retrieved.


### -param pServerPrincName [out, optional]

The current principal name. The string will be allocated by the callee using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, and must be freed by the caller using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. By default, Schannel principal names will be in the msstd form. The fullsic form will be returned if EOAC_MAKE_FULLSIC is specified in the <i>pCapabilities</i> parameter. For more information about the msstd and fullsic forms, see <a href="https://msdn.microsoft.com/4d9977f8-0efb-4559-977e-3eba4e277bc0">Principal Names</a>. If the caller specifies <b>NULL</b>, the current principal name is not retrieved.


### -param pAuthnLevel [out, optional]

A pointer to a variable that receives the current authentication level. This will be a single value taken from the <a href="https://msdn.microsoft.com/06c409e4-3772-45cf-8c31-c64f99aca244">authentication level constants</a>. If the caller specifies <b>NULL</b>, the current authentication level is not retrieved.


### -param pImpLevel [out, optional]

This parameter must be <b>NULL</b>.


### -param pPrivs [out, optional]

A pointer to a handle that receives the privilege information for the client application. The format of the structure that the handle refers to depends on the authentication service. The application should not write or free the memory. The information is valid only for the duration of the current call. For NTLMSSP and Kerberos, this is a string identifying the client principal. For Schannel, this is a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the client's certificate. If the client has no certificate, <b>NULL</b> is returned. If the caller specifies <b>NULL</b>, the current privilege information is not retrieved. See <a href="https://msdn.microsoft.com/35b6a3f4-1703-4244-98fd-fad7de48b262">RPC_AUTHZ_HANDLE</a>.


### -param pCapabilities [in, out, optional]

A pointer to return flags indicating capabilities of the call. To request that the principal name be returned in fullsic form if Schannel is the authentication service, the caller can set the EOAC_MAKE_FULLSIC flag in this parameter. If the caller specifies <b>NULL</b>, the current capabilities are not retrieved.


## -returns



This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -remarks



<b>CoQueryClientBlanket</b> is called by the server to get security information about the client that invoked the method executing on the current thread. This function encapsulates the following sequence of common calls (error handling excluded):



<pre class="syntax" xml:space="preserve"><code>    CoGetCallContext(IID_IServerSecurity, (void**)&amp;pss);
    pss-&gt;QueryBlanket(pAuthnSvc, pAuthzSvc, pServerPrincName, 
                pAuthnLevel, pImpLevel, pPrivs, pCapabilities);
    pss-&gt;Release();
</code></pre>
This sequence calls <a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a> to get a pointer to <a href="https://msdn.microsoft.com/aacef77c-7185-44ed-aa1a-465c6100a431">IServerSecurity</a> and, with the resulting pointer, calls <a href="https://msdn.microsoft.com/1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868">IServerSecurity::QueryBlanket</a> and then releases the pointer.




## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/e613e06a-0900-413e-bde2-39ce1612fed1">CoQueryProxyBlanket</a>



<a href="https://msdn.microsoft.com/1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868">IServerSecurity::QueryBlanket</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

