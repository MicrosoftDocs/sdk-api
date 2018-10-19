---
UID: NC:wincrypt.PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC
title: PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC
author: windows-sdk-content
description: Called by CryptImportPublicKeyInfoEx2 to decode the public key algorithm identifier, load the algorithm provider, and import the key pair.
old-location: security\pfn_import_public_key_info_ex2_func.htm
tech.root: seccrypto
ms.assetid: b8d26a54-1549-4d2b-9cd6-c551407d795d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC, PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC callback, PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function [Security], X509_ASN_ENCODING, security.pfn_import_public_key_info_ex2_func, wincrypt/PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC callback function


## -description


The <b>PFN_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC</b> callback function is called by <a href="https://msdn.microsoft.com/c73f2499-75e9-4146-ae4c-0e949206ea37">CryptImportPublicKeyInfoEx2</a> to decode the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a> identifier, load the algorithm provider, and import the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key pair</a>.


## -parameters




### -param dwCertEncodingType [in]

The <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate encoding type</a> that was used to encrypt the subject. The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


This parameter can be the following currently defined certificate encoding type.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate encoding.

</td>
</tr>
</table>
 


### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> information to import into the provider.


### -param dwFlags [in]

A set of flags that modify the behavior of this function. This can be zero.


### -param *pvAuxInfo [in]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param *phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> variable that receives the handle of the imported key.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You can use <a href="cryptography_functions.htm">OID Support Functions</a> to deploy this callback function. Wincrypt.h defines the following constant for this purpose.

<table>
<tr>
<th>Constant</th>
<th>Definition</th>
</tr>
<tr>
<td>CRYPT_OID_IMPORT_PUBLIC_KEY_INFO_EX2_FUNC</td>
<td>"CryptDllImportPublicKeyInfoEx2"</td>
</tr>
</table>
 



