---
UID: NF:wincrypt.CertFindSubjectInCTL
title: CertFindSubjectInCTL function (wincrypt.h)
description: The CertFindSubjectInCTL function attempts to find the specified subject in a certificate trust list (CTL).
helpviewer_keywords: ["CTL_ANY_SUBJECT_TYPE","CTL_CERT_SUBJECT_TYPE","CertFindSubjectInCTL","CertFindSubjectInCTL function [Security]","_crypto2_certfindsubjectinctl","security.certfindsubjectinctl","wincrypt/CertFindSubjectInCTL"]
old-location: security\certfindsubjectinctl.htm
tech.root: security
ms.assetid: e0c81531-e649-45bb-bafe-bced00c7b16a
ms.date: 12/05/2018
ms.keywords: CTL_ANY_SUBJECT_TYPE, CTL_CERT_SUBJECT_TYPE, CertFindSubjectInCTL, CertFindSubjectInCTL function [Security], _crypto2_certfindsubjectinctl, security.certfindsubjectinctl, wincrypt/CertFindSubjectInCTL
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertFindSubjectInCTL
 - wincrypt/CertFindSubjectInCTL
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
 - CertFindSubjectInCTL
---

# CertFindSubjectInCTL function


## -description

The <b>CertFindSubjectInCTL</b> function attempts to find the specified subject in a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL). A subject can be identified either by the certificate's whole context or by any unique identifier of the certificate's subject such as the SHA1 <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the certificate's issuer and serial number.

## -parameters

### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param dwSubjectType [in]

Specifies the type of subject to be searched for in the CTL. May be <b>NULL</b> for a default search.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTL_CERT_SUBJECT_TYPE"></a><a id="ctl_cert_subject_type"></a><dl>
<dt><b>CTL_CERT_SUBJECT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> data type: Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

The CTL's <b>SubjectAlgorithm</b> is examined to determine the representation of the subject's identity. Initially, only SHA1 and MD5 hashes are supported as values for <b>SubjectAlgorithm</b>. The appropriate hash property is obtained from the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_ANY_SUBJECT_TYPE"></a><a id="ctl_any_subject_type"></a><dl>
<dt><b>CTL_ANY_SUBJECT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
<i>pvSubject</i> data type: Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a> structure.

The <b>SubjectAlgorithm</b> member of this structure must match the algorithm type of the CTL, and the <b>SubjectIdentifier</b> member must match one of the CTL entries.

</td>
</tr>
</table>
 

The certificate's <a href="/windows/desktop/SecGloss/h-gly">hash</a> or the <b>SubjectIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a> structure is used as the key in searching the subject entries. A binary memory comparison is done between the key and the entry's SubjectIdentifier.

If <i>dwSubjectType</i> is set to either preceding value, <i>dwEncodingType</i> is not used.

### -param pvSubject [in]

Pointer used in conjunction with the <i>dwSubjectType</i> parameter.

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure being searched.

### -param dwFlags [in]

Reserved for future use and must be zero.

## -returns

If the function succeeds, the return value is the entry, if it is found.

If the function fails, the return value is <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The subject was not found in the CTL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSubjectType</i> parameter was not either CTL_CERT_SUBJECT_TYPE or CTL_ANY_SUBJECT_TYPE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The CTL's <b>SubjectAlgorithm</b> member did not map to either SHA1 or MD5.

</td>
</tr>
</table>

## -remarks

The certificate's hash or the <b>SubjectIdentifier</b> member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a> structure is used as the key in searching the subject entries. A binary memory comparison is done between the key and the entry's <b>SubjectIdentifier</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate and Certificate Store Maintenance Functions</a>