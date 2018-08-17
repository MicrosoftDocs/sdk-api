---
UID: NF:wincrypt.CertCloseStore
title: CertCloseStore function
author: windows-sdk-content
description: Closes a certificate store handle and reduces the reference count on the store.
old-location: security\certclosestore.htm
old-project: SecCrypto
ms.assetid: a93fdd65-359e-4046-910d-347c3af01280
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: CERT_CLOSE_STORE_CHECK_FLAG, CERT_CLOSE_STORE_FORCE_FLAG, CertCloseStore, CertCloseStore function [Security], _crypto2_certclosestore, security.certclosestore, wincrypt/CertCloseStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCloseStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertCloseStore function


## -description


The <b>CertCloseStore</b> function closes a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> handle and reduces the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the store. There needs to be a corresponding call to <b>CertCloseStore</b> for each successful call to the 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> or 
<a href="https://msdn.microsoft.com/628efd30-6e07-4748-82ac-5cdc723be451">CertDuplicateStore</a> functions.


## -parameters




### -param hCertStore [in]

Handle of the certificate store to be closed.


### -param dwFlags [in]

Typically, this parameter uses the default value zero. The default is to close the store with memory remaining allocated for contexts that have not been freed. In this case, no check is made to determine whether memory for contexts remains allocated. 




Set flags can force the freeing of memory for all of a store's <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL), and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) contexts when the store is closed. Flags can also be set that check whether all of the store's certificate, CRL, and CTL contexts have been freed. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CLOSE_STORE_CHECK_FLAG"></a><a id="cert_close_store_check_flag"></a><dl>
<dt><b>CERT_CLOSE_STORE_CHECK_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Checks for nonfreed certificate, CRL, and CTL contexts. A returned error code indicates that one or more store elements is still in use. This flag should only be used as a diagnostic tool in the development of applications.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CLOSE_STORE_FORCE_FLAG"></a><a id="cert_close_store_force_flag"></a><dl>
<dt><b>CERT_CLOSE_STORE_FORCE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Forces the freeing of memory for all contexts associated with the store. This flag can be safely used only when the store is opened in a function and neither the store handle nor any of its contexts are passed to any called functions. For details, see  Remarks.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If CERT_CLOSE_STORE_CHECK_FLAG is not set or if it is set and all contexts associated with the store have been freed, the return value is <b>TRUE</b>.

If CERT_CLOSE_STORE_CHECK_FLAG is set and memory for one or more contexts associated with the store remains allocated, the return value is <b>FALSE</b>. The store is always closed even when the function returns <b>FALSE</b>. For details, see  Remarks.


<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> is set to CRYPT_E_PENDING_CLOSE if memory for contexts associated with the store remains allocated. Any existing value returned by <b>GetLastError</b> is preserved unless CERT_CLOSE_STORE_CHECK_FLAG is set.




## -remarks



While a certificate store is open, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">contexts</a> from that store can be retrieved or duplicated. When a <i>context</i> is retrieved or duplicated, its reference count is incremented. When a context is freed by passing it to a search or enumeration function as a previous context or by using 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>, 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>, or 
<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>, its reference count is decremented. When a context's reference count reaches zero, memory allocated for that context is automatically freed. When the memory allocated for a context has been freed, any pointers to that context become not valid.

By default, memory used to store contexts with reference count greater than zero is not freed when a certificate store is closed. References to those contexts remain valid; however, this can cause memory leaks. Also, any changes made to the properties of a context after the store has been closed are not persisted.

To force the freeing of memory for all contexts associated with a store, set CERT_CLOSE_STORE_FORCE_FLAG. With this flag set, memory for all contexts associated with the store is freed and all pointers to certificate, CRL, or CTL contexts associated with the store become not valid. This flag should only be set when the store is opened in a function and neither the store handle nor any of its contexts were ever passed to any called functions.

The status of reference counts on contexts associated with a store can be checked when the store is closed by using CERT_CLOSE_STORE_CHECK_FLAG. When this flag is set, and all certificate, CRL, or CTL contexts have not been released, the function returns <b>FALSE</b> and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns CRYPT_E_PENDING_CLOSE. Note that the store is still closed when <b>FALSE</b> is returned and the memory for any active contexts is not freed.

If CERT_STORE_NO_CRYPT_RELEASE_FLAG was not set when the store was opened, closing a store releases its CSP handle.




## -see-also




<a href="https://msdn.microsoft.com/628efd30-6e07-4748-82ac-5cdc723be451">CertDuplicateStore</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="https://msdn.microsoft.com/84b1aa0c-44d9-4a2f-861c-fa7d8caac192">CertFreeCTLContext</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>



<a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a>
 

 

