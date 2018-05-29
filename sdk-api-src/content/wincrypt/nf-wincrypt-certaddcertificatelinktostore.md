---
UID: NF:wincrypt.CertAddCertificateLinkToStore
title: CertAddCertificateLinkToStore function
author: windows-sdk-content
description: Adds a link in a certificate store to a certificate context in a different store.
old-location: security\certaddcertificatelinktostore.htm
old-project: SecCrypto
ms.assetid: bcbf7755-d0ce-4dd5-8462-72760364fdc3
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_USE_EXISTING, CertAddCertificateLinkToStore, CertAddCertificateLinkToStore function [Security], _crypto2_certaddcertificatelinktostore, security.certaddcertificatelinktostore, wincrypt/CertAddCertificateLinkToStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertAddCertificateLinkToStore
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertAddCertificateLinkToStore function


## -description


The <b>CertAddCertificateLinkToStore</b> function adds a link in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> in a different store. Instead of creating and adding a duplicate of the certificate context, this function adds a link to the original certificate.


## -parameters




### -param hCertStore [in]

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> where the link is to be added.


### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure to be linked.


### -param dwAddDisposition [in]

Specifies the action if a matching certificate or a link to a matching certificate already exists in the store. Currently defined disposition values and their uses are as follows. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_ALWAYS"></a><a id="cert_store_add_always"></a><dl>
<dt><b>CERT_STORE_ADD_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
The function makes no check for an existing matching certificate or link to a matching certificate. A new certificate is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists, the operation fails. 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a link to a matching certificate exists, that existing link is deleted and a new link is created and added to the store. If no matching certificate or link to a matching certificate exists, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists, the existing certificate is used. The function does not fail, but no new link is added. If no matching certificate or link to a matching certificate exists, a new link is added.

</td>
</tr>
</table>
 


### -param ppStoreContext [out, optional]

A pointer to a pointer to a copy of the link created. The <i>ppStoreContext</i> parameter can be <b>NULL</b> to indicate that a copy of the link is not needed. If a copy of the link is created, that copy must be freed using 
the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
For a <i>dwAddDisposition</i> parameter of CERT_STORE_ADD_NEW, the certificate already exists in the store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A disposition value that is not valid was specified in the <i>dwAddDisposition</i> parameter.

</td>
</tr>
</table>
 




## -remarks



Because the link provides access to the original certificate <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>, setting an extended property in the linked <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> changes that extended property in the certificate's original location and in any other links to that certificate.

Links cannot be added to a store opened as a collection. Stores opened as collections include all stores opened with 
<a href="https://msdn.microsoft.com/23699439-1a6c-4907-93fa-651024856be7">CertOpenSystemStore</a> or 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> using CERT_STORE_PROV_SYSTEM or CERT_STORE_PROV_COLLECTION. For more information, see 
<a href="https://msdn.microsoft.com/ea848d74-c3ec-4166-90ea-121b33f7f318">CertAddStoreToCollection</a>.

If links are used and 
<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> is called with CERT_CLOSE_STORE_FORCE_FLAG, the store that uses links must be closed before the store that contains the original contexts is closed. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the two stores can be closed in either order.

To remove the certificate context link from the certificate store, use the  <a href="https://msdn.microsoft.com/4390c8da-9c4d-47a4-9af4-d179829f77f3">CertDeleteCertificateFromStore</a> function.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/cf87791c-b98c-4dd7-b346-336c4b1a88ca">Example C Program: Certificate Store Operations</a>. For additional code that uses this function, see <a href="https://msdn.microsoft.com/5349222f-ad68-477c-8712-fde16e68f600">Example C Program: Collection and Sibling Certificate Store Operations</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2fde63ed-7522-4400-a16b-059a001e7c26">CertAddCRLLinkToStore</a>



<a href="https://msdn.microsoft.com/c129aeae-69d9-440a-979d-e9e481c64538">CertAddCTLLinkToStore</a>



<a href="https://msdn.microsoft.com/ea848d74-c3ec-4166-90ea-121b33f7f318">CertAddStoreToCollection</a>



<a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>



<a href="https://msdn.microsoft.com/23699439-1a6c-4907-93fa-651024856be7">CertOpenSystemStore</a>



<a href="cryptography_functions.htm">Certificate Functions</a>
 

 

