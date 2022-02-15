---
UID: NF:mssip.CryptSIPGetSignedDataMsg
title: CryptSIPGetSignedDataMsg function (mssip.h)
description: Retrieves an Authenticode signature from the file.
helpviewer_keywords: ["CryptSIPGetSignedDataMsg","CryptSIPGetSignedDataMsg function [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","mssip/CryptSIPGetSignedDataMsg","security.cryptsipgetsigneddatamsg"]
old-location: security\cryptsipgetsigneddatamsg.htm
tech.root: security
ms.assetid: e3fabaa7-2dda-4c6c-8d1a-3ee5363e10b5
ms.date: 12/05/2018
ms.keywords: CryptSIPGetSignedDataMsg, CryptSIPGetSignedDataMsg function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, mssip/CryptSIPGetSignedDataMsg, security.cryptsipgetsigneddatamsg
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptSIPGetSignedDataMsg
 - mssip/CryptSIPGetSignedDataMsg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPGetSignedDataMsg
---

# CryptSIPGetSignedDataMsg function


## -description

The <b>CryptSIPGetSignedDataMsg</b> function retrieves an <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> signature from the file.

## -parameters

### -param pSubjectInfo [in]

A pointer to a [SIP_SUBJECTINFO](/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo) structure that contains information about the message subject.

### -param pdwEncodingType [out]

The encoding type of the Authenticode signature.


This parameter can be a combination of one or more of the following values.



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
Specifies <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> message encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
</table>

### -param dwIndex [in]

This parameter is reserved and should be set to zero.

### -param pcbSignedDataMsg [in, out]

The length, in bytes, of the buffer pointed to by the <i>pbSignedDataMsg</i> parameter.

### -param pbSignedDataMsg [out]

A pointer to a buffer to receive the returned Authenticode signature. 

To determine the size of the buffer needed, set the <i>pbSignedDataMsg</i> parameter to <b>NULL</b> and call the <b>CryptSIPGetSignedDataMsg</b> function. This function will place the required size of the buffer, in bytes, in the value pointed to by <i>pcbSignedDataMsg</i>. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
The signature specified by the index could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The specified data or file format of the <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The [SIP_SUBJECTINFO](/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo) structure is a null pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the message buffer was insufficient to hold the retrieved data, the <i>pcbSignedDataMsg</i> parameter has been set to indicate the required buffer size.

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

Subjects include, but are not limited to, portable executable images (.exe), cabinet (.cab) images, flat files, and catalog files. Each subject type uses a different subset of its data for hash calculation and requires a different procedure for storage and retrieval. Therefore, each subject type has a unique SIP specification.

## -see-also

<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipputsigneddatamsg">CryptSIPPutSignedDataMsg</a>



<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremovesigneddatamsg">CryptSIPRemoveSignedDataMsg</a>