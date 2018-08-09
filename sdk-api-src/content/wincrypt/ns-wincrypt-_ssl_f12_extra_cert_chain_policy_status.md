---
UID: NS:wincrypt._SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
title: "_SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS"
author: windows-sdk-content
description: The SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS structure checks if any certificates in the chain have weak cryptography and checks if a third party root certificate is compliant with the Microsoft Root Program requirements.
old-location: security\ssl_f12_extra_cert_chain_policy_status.htm
old-project: seccrypto
ms.assetid: A78598AA-1C5F-49E9-9A0D-6B6C838F7DDD
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, CERT_CHAIN_POLICY_SSL_F12_ERROR_LEVEL, CERT_CHAIN_POLICY_SSL_F12_NONE_CATEGORY, CERT_CHAIN_POLICY_SSL_F12_ROOT_PROGRAM_CATEGORY, CERT_CHAIN_POLICY_SSL_F12_SUCCESS_LEVEL, CERT_CHAIN_POLICY_SSL_F12_WARNING_LEVEL, CERT_CHAIN_POLICY_SSL_F12_WEAK_CRYPTO_CATEGORY, PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS structure pointer [Security], SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS structure [Security], _SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, security.ssl_f12_extra_cert_chain_policy_status, wincrypt/PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, wincrypt/SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

The <b>SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS</b> structure checks if any certificates in the chain have weak  cryptography and checks if a third party root certificate is compliant with the Microsoft Root Program requirements. An error string will be provided if either condition is not met.


## -struct-fields




### -field cbSize

<b>DWORD</b> value that specifies the size, in bytes, of this structure. This value must be set to a value greater than or equal to sizeof(SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS).


### -field dwErrorLevel

<b>DWORD</b> value that specifies the level of an error.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_SUCCESS_LEVEL"></a><a id="cert_chain_policy_ssl_f12_success_level"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_SUCCESS_LEVEL</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No certificate errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_WARNING_LEVEL"></a><a id="cert_chain_policy_ssl_f12_warning_level"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_WARNING_LEVEL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Certificate warning level.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_ERROR_LEVEL"></a><a id="cert_chain_policy_ssl_f12_error_level"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_ERROR_LEVEL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Certificate error level.

</td>
</tr>
</table>
 


### -field dwErrorCategory

<b>DWORD</b> value that specifies the category of an error. Each error category has a corresponding <b>dwErrorLevel</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_NONE_CATEGORY"></a><a id="cert_chain_policy_ssl_f12_none_category"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_NONE_CATEGORY</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No certificate errors.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_WEAK_CRYPTO_CATEGORY"></a><a id="cert_chain_policy_ssl_f12_weak_crypto_category"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_WEAK_CRYPTO_CATEGORY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Errors in this category with the <b>dwErrorLevel</b>: <b>CERT_CHAIN_POLICY_SSL_F12_WARNING_LEVEL</b> are errors associated with all other roots including enterprise.

Errors in this category with the <b>dwErrorLevel</b>: <b>CERT_CHAIN_POLICY_SSL_F12_ERROR_LEVEL</b> are errors associated with the third party root certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_POLICY_SSL_F12_ROOT_PROGRAM_CATEGORY"></a><a id="cert_chain_policy_ssl_f12_root_program_category"></a><dl>
<dt><b>CERT_CHAIN_POLICY_SSL_F12_ROOT_PROGRAM_CATEGORY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Errors in this category with the <b>dwErrorLevel</b>: <b>CERT_CHAIN_POLICY_SSL_F12_WARNING_LEVEL</b> are all errors with root program compliance failures.

</td>
</tr>
</table>
 


### -field dwReserved

<b>DWORD</b> value reserved for future use.


### -field wszErrorText

The error string provided if any certificates in the chain have weak cryptography or if the third party root certificate is not compliant with the Microsoft Root Program requirements.


## -see-also




<a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a>
 

 

