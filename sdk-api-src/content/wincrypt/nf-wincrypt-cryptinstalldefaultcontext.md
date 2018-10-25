---
UID: NF:wincrypt.CryptInstallDefaultContext
title: CryptInstallDefaultContext function
author: windows-sdk-content
description: Installs a specific provider to be the default context provider for the specified algorithm.
old-location: security\cryptinstalldefaultcontext.htm
tech.root: seccrypto
ms.assetid: 79d121df-0699-424e-a8de-5fc2b396afc2
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CRYPT_DEFAULT_CONTEXT_AUTO_RELEASE_FLAG, CRYPT_DEFAULT_CONTEXT_CERT_SIGN_OID, CRYPT_DEFAULT_CONTEXT_MULTI_CERT_SIGN_OID, CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG, CryptInstallDefaultContext, CryptInstallDefaultContext function [Security], _crypto2_cryptinstalldefaultcontext, security.cryptinstalldefaultcontext, wincrypt/CryptInstallDefaultContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptInstallDefaultContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptInstallDefaultContext function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptInstallDefaultContext</b> function installs a specific provider to be the default <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> provider for the specified algorithm.


## -parameters




### -param hCryptProv [in]

The handle of the cryptographic service provider to be used as the default context. This handle is obtained by using the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function.


### -param dwDefaultType [in]

Specifies the type of context to install. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DEFAULT_CONTEXT_CERT_SIGN_OID"></a><a id="crypt_default_context_cert_sign_oid"></a><dl>
<dt><b>CRYPT_DEFAULT_CONTEXT_CERT_SIGN_OID</b></dt>
</dl>
</td>
<td width="60%">
Installs the default provider used to verify a single certificate signature type. 

The <i>pvDefaultPara</i> parameter is the address of a null-terminated ANSI string that contains the object identifier of the certificate signature algorithm to install the provider for, for example, <b>szOID_OIWSEC_md5RSA</b>. If the <i>pvDefaultPara</i> parameter is <b>NULL</b>, the specified provider is used to verify all certificate signatures. The <i>pvDefaultPara</i> parameter cannot be <b>NULL</b> when the <b>CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG</b> flag is set.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DEFAULT_CONTEXT_MULTI_CERT_SIGN_OID"></a><a id="crypt_default_context_multi_cert_sign_oid"></a><dl>
<dt><b>CRYPT_DEFAULT_CONTEXT_MULTI_CERT_SIGN_OID</b></dt>
</dl>
</td>
<td width="60%">
Installs the default provider used to verify multiple certificate signature types. 

The <i>pvDefaultPara</i> parameter is the address of a <a href="https://msdn.microsoft.com/2826ee4f-55b7-4161-8698-3a9b59190dcc">CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA</a> structure that contains an array of object identifiers that identify the certificate signature algorithms to install the specified provider for.

</td>
</tr>
</table>
 


### -param pvDefaultPara [in]

Specifies the object or objects to install the default context provider for. The format of this parameter depends on the contents of the <i>dwDefaultType</i> parameter.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DEFAULT_CONTEXT_AUTO_RELEASE_FLAG"></a><a id="crypt_default_context_auto_release_flag"></a><dl>
<dt><b>CRYPT_DEFAULT_CONTEXT_AUTO_RELEASE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The provider handle specified by the <i>hCryptProv</i> parameter is released automatically when the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> or thread ends. If this flag is not specified, it is the caller's responsibility to release the provider handle by using the <a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a> function when the handle is no longer needed. The provider handle is not released if the <a href="https://msdn.microsoft.com/ad7be5cf-f078-4a9f-81c4-959e4203dba8">CryptUninstallDefaultContext</a> function is called before the process or thread exits.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG"></a><a id="crypt_default_context_process_flag"></a><dl>
<dt><b>CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The provider applies to all threads in the process. If this flag is not specified, the provider only applies to the calling thread. The <i>pvDefaultPara</i> parameter cannot be <b>NULL</b> when this flag is set.

</td>
</tr>
</table>
 


### -param pvReserved [in]

This parameter is reserved for future use.


### -param phDefaultContext [out]

The address of an <b>HCRYPTDEFAULTCONTEXT</b> variable that receives the default context handle. This handle is passed to the <a href="https://msdn.microsoft.com/ad7be5cf-f078-4a9f-81c4-959e4203dba8">CryptUninstallDefaultContext</a> function to uninstall the default context provider.


## -returns



If the function succeeds, the return value is nonzero (TRUE). If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The installed default context providers are stack ordered, thus when searching for a default context provider, the system starts with the most recently installed provider. The per-thread list of providers is searched before the per-process list of providers. After a match is found, the system does not continue to search for other matches.

The installed provider handle must remain available for use until <a href="https://msdn.microsoft.com/ad7be5cf-f078-4a9f-81c4-959e4203dba8">CryptUninstallDefaultContext</a> is called, or the thread or <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> exits.




## -see-also




<a href="https://msdn.microsoft.com/ad7be5cf-f078-4a9f-81c4-959e4203dba8">CryptUninstallDefaultContext</a>
 

 

