---
UID: NF:mssip.CryptSIPPutSignedDataMsg
title: CryptSIPPutSignedDataMsg function (mssip.h)
author: windows-sdk-content
description: Stores an Authenticode signature in the target file.
old-location: security\cryptsipputsigneddatamsg.htm
tech.root: SecCrypto
ms.assetid: 731f64bf-49f0-4799-b84a-9ca04292aa91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptSIPPutSignedDataMsg, CryptSIPPutSignedDataMsg function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, mssip/CryptSIPPutSignedDataMsg, security.cryptsipputsigneddatamsg
ms.topic: function
f1_keywords: ["mssip/CryptSIPPutSignedDataMsg"]
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
 - CryptSIPPutSignedDataMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptSIPPutSignedDataMsg function


## -description


The <b>CryptSIPPutSignedDataMsg</b> function stores an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Authenticode</a> signature in the target file.


## -parameters




### -param pSubjectInfo [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a> structure that contains information about the message subject.


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
Specifies <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">PKCS #7</a> message encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="https://docs.microsoft.com/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

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

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.



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
The specified data or file format of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) is not valid.

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
<li>The <i>cbSignedDataMsg</i> value is greater than the <b>cbSize</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a> structure.</li>
<li>The <i>dwEncodingType</i> parameter value is greater than the <b>dwEncodingType</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a> structure.</li>
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




<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipgetsigneddatamsg">CryptSIPGetSignedDataMsg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipremovesigneddatamsg">CryptSIPRemoveSignedDataMsg</a>
 

 

