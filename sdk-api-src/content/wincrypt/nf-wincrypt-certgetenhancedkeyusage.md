---
UID: NF:wincrypt.CertGetEnhancedKeyUsage
title: CertGetEnhancedKeyUsage function
author: windows-sdk-content
description: Returns information from the enhanced key usage (EKU) extension or the EKU extended property of a certificate.
old-location: security\certgetenhancedkeyusage.htm
tech.root: seccrypto
ms.assetid: eda6d875-df62-4f40-8734-a91666dba289
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG, CERT_FIND_PROP_ONLY_ENHKEY_USAGE_FLAG, CertGetEnhancedKeyUsage, CertGetEnhancedKeyUsage function [Security], _crypto2_certgetenhancedkeyusage, security.certgetenhancedkeyusage, wincrypt/CertGetEnhancedKeyUsage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
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
 - CertGetEnhancedKeyUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CertGetEnhancedKeyUsage
: 
---

# CertGetEnhancedKeyUsage function


## -description


The <b>CertGetEnhancedKeyUsage</b> function returns information from the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enhanced key usage</a> (EKU) extension or the EKU extended property of a certificate. EKUs indicate valid uses of the certificate.


## -parameters




### -param pCertContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> certificate context.


### -param dwFlags [in]

Indicates whether the function will report on extensions of a certificate, its extended properties, or both. If set to zero, the function returns the valid uses of a certificate based on both the EKU extension and the EKU extended property value of the certificate. 




To return only the EKU extension or EKU property value, set the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG"></a><a id="cert_find_ext_only_enhkey_usage_flag"></a><dl>
<dt><b>CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Get only the extension.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PROP_ONLY_ENHKEY_USAGE_FLAG"></a><a id="cert_find_prop_only_enhkey_usage_flag"></a><dl>
<dt><b>CERT_FIND_PROP_ONLY_ENHKEY_USAGE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Get only the extended property value.

</td>
</tr>
</table>
 


### -param pUsage [out]

A pointer to a <a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CERT_ENHKEY_USAGE</a> structure (<b>CERT_ENHKEY_USAGE</b> is an alternate typedef name for the <b>CTL_USAGE</b> structure) that receives the valid uses of the certificate. 




This parameter can be <b>NULL</b> to set the size of the key usage for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbUsage [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the structure pointed to by <i>pUsage</i>. When the function returns, the <b>DWORD</b> contains the size, in bytes, of the structure.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).




## -remarks



If a certificate has an EKU extension, that extension lists <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) for valid uses of that certificate. In a Microsoft environment, a certificate might also have EKU extended properties that specify valid uses for the certificate.

<ul>
<li>If a certificate has neither an EKU extension nor EKU extended properties, it is assumed to be valid for all uses.</li>
<li>If it has either an EKU extension or EKU extended properties but not both, it is valid only for the uses indicated in the extension or extended properties that it has.</li>
<li>If a certificate has both an EKU extension and EKU extended properties, it is valid only for the uses that are on both lists.</li>
</ul>
If <i>dwFlags</i> is set to zero, the <b>cUsageIdentifier</b> member of the <b>CERT_ENHKEY_USAGE</b> structure is set to the number of valid uses of the certificate determined by the value of both the EKU extension and the EKU extended property value.

If the <b>cUsageIdentifier</b> member is zero, the certificate might be valid for all uses or the certificate might have no valid uses. The return from a call to <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> can be used to determine whether the certificate is good for all uses or for none. If <b>GetLastError</b> returns CRYPT_E_NOT_FOUND, the certificate is good for all uses. If it returns zero, the certificate has no valid uses.




## -see-also




<a href="https://msdn.microsoft.com/423b0232-846e-4e40-bc42-d30c48c548da">CertSetEnhancedKeyUsage</a>



<a href="cryptography_functions.htm">Enhanced Key Usage Functions</a>
 

 

