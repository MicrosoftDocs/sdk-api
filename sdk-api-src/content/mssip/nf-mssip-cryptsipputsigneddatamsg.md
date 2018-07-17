---
UID: NF:mssip.CryptSIPPutSignedDataMsg
title: CryptSIPPutSignedDataMsg function
author: windows-sdk-content
description: Stores an Authenticode signature in the target file.
old-location: security\cryptsipputsigneddatamsg.htm
old-project: SecCrypto
ms.assetid: 731f64bf-49f0-4799-b84a-9ca04292aa91
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CryptSIPPutSignedDataMsg, CryptSIPPutSignedDataMsg function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, mssip/CryptSIPPutSignedDataMsg, security.cryptsipputsigneddatamsg
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mssip.h
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
tech.root: 
req.typenames: SimilarityFileId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPPutSignedDataMsg
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CryptSIPPutSignedDataMsg function


## -description


The <b>CryptSIPPutSignedDataMsg</b> function stores an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> signature in the target file.


## -parameters




### -param pSubjectInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure that contains information about the message subject.


### -param dwEncodingType [in]

The encoding type of the message. This can be a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PKCS_7_ASN_ENCODING"></a><a id="pkcs_7_asn_encoding"></a><dl>
<dt><b>PKCS_7_ASN_ENCODING</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #7</a> message encoding.

</td>
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
 


### -param pdwIndex [out]

Pointer to the message index.


### -param cbSignedDataMsg [in]

Length, in bytes, of the buffer pointed to by the <i>pbSignedDataMsg</i> parameter.


### -param pbSignedDataMsg [in]

Pointer to the buffer that contains the message. 


## -returns




If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The specified data or file format of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
This code can be returned for the following reasons:

<ul>
<li>The <i>pSubjectInfo</i> is <b>NULL</b>.</li>
<li>The <i>pdwIndex</i> is <b>NULL</b>.</li>
<li>The <i>pbSignedDataMsg</i> is <b>NULL</b>.</li>
<li>The value of the <i>cbSignedDataMsg</i> parameter is less than one.</li>
<li>The <i>cbSignedDataMsg</i> value is greater than the <b>cbSize</b> member of the <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure.</li>
<li>The <i>dwEncodingType</i> parameter value is greater than the <b>dwEncodingType</b> member of the <a href="https://msdn.microsoft.com/6274cd08-d67f-410d-9303-3a42b7f1edc6">SIP_SUBJECTINFO</a> structure.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_FORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The specified subject type is not valid.

</td>
</tr>
</table>
 




## -remarks



Each subject type uses a different subset of its data for hash calculation and requires a different procedure for storage and retrieval. Therefore, each subject type has a unique SIP specification.




## -see-also




<a href="https://msdn.microsoft.com/e3fabaa7-2dda-4c6c-8d1a-3ee5363e10b5">CryptSIPGetSignedDataMsg</a>



<a href="https://msdn.microsoft.com/c3ea46bb-931a-4ca6-93f5-db7e07b4cb7a">CryptSIPRemoveSignedDataMsg</a>
 

 

