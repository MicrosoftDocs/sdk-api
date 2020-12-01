---
UID: NF:wincrypt.CertFindCTLInStore
title: CertFindCTLInStore function (wincrypt.h)
description: Finds the first or next certificate trust list (CTL) context that matches search criteria established by the dwFindType and its associated pvFindPara.
helpviewer_keywords: ["CTL_FIND_ANY","CTL_FIND_EXISTING","CTL_FIND_MD5_HASH","CTL_FIND_SAME_USAGE_FLAG","CTL_FIND_SHA1_HASH","CTL_FIND_SUBJECT","CTL_FIND_USAGE","CertFindCTLInStore","CertFindCTLInStore function [Security]","_crypto2_certfindctlinstore","security.certfindctlinstore","wincrypt/CertFindCTLInStore"]
old-location: security\certfindctlinstore.htm
tech.root: security
ms.assetid: e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c
ms.date: 12/05/2018
ms.keywords: CTL_FIND_ANY, CTL_FIND_EXISTING, CTL_FIND_MD5_HASH, CTL_FIND_SAME_USAGE_FLAG, CTL_FIND_SHA1_HASH, CTL_FIND_SUBJECT, CTL_FIND_USAGE, CertFindCTLInStore, CertFindCTLInStore function [Security], _crypto2_certfindctlinstore, security.certfindctlinstore, wincrypt/CertFindCTLInStore
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
 - CertFindCTLInStore
 - wincrypt/CertFindCTLInStore
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
 - CertFindCTLInStore
---

# CertFindCTLInStore function


## -description

The <b>CertFindCTLInStore</b> function finds the first or next <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) <a href="/windows/desktop/SecGloss/c-gly">context</a> that matches search criteria established by the <i>dwFindType</i> and its associated <i>pvFindPara</i>. This function can be used in a loop to find all of the CTL contexts in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that match the specified find criteria.

## -parameters

### -param hCertStore [in]

Handle of the certificate store to be searched.

### -param dwMsgAndCertEncodingType [in]

Specifies the type of encoding used on the CTL. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>


This parameter is used only when the <i>dwFindType</i> parameter is set to CTL_FIND_USAGE.

### -param dwFindFlags [in]

Can be set when <i>dwFindType</i> is set to CTL_FIND_USAGE. For details, see the comments under CTL_FIND_USAGE, following.

### -param dwFindType [in]

Specifies the type of search being made. The search type determines the data type, contents, and the use of <i>pvFindPara</i>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_ANY"></a><a id="ctl_find_any"></a><dl>
<dt><b>CTL_FIND_ANY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>NULL</b>.

Any CTL is a match.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SHA1_HASH"></a><a id="ctl_find_sha1_hash"></a><dl>
<dt><b>CTL_FIND_SHA1_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

A CTL with a hash matching the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure is found.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_MD5_HASH"></a><a id="ctl_find_md5_hash"></a><dl>
<dt><b>CTL_FIND_MD5_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

A CTL with a hash matching the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure is found.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_USAGE"></a><a id="ctl_find_usage"></a><dl>
<dt><b>CTL_FIND_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a>.

Any CTL is found that has a usage identifier, list identifier, or signer matching the usage identifier, list identifier, or signer in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a> structure.

If the <b>cUsageIdentifier</b> member is of <b>SubjectUsage</b> size, any CTL is a match.

If the <b>cbData</b> member of <b>ListIdentifier</b> member is zero, any list identifier is a match. If the <b>cbData</b> member of <b>ListIdentifier</b> is CTL_FIND_NO_LIST_ID_CBDATA, only a CTL without a list identifier is a match.

If the <b>pSigner</b> member in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a> structure is <b>NULL</b>, any CTL signer is a match, and only the <b>Issuer</b> and <b>SerialNumber</b> members in the <b>pSigner</b> <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure are used. If <b>pSigner</b> is CTL_FIND_NO_SIGNER_PTR, only a CTL without a signer is a match.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SAME_USAGE_FLAG"></a><a id="ctl_find_same_usage_flag"></a><dl>
<dt><b>CTL_FIND_SAME_USAGE_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a>.

Only CTLs with exactly the same usage identifiers are matched. CTLs having additional usage identifiers are not matched. For example, if only "1.2.3" is specified in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a> structure, then for a match, the CTL must only contain "1.2.3" and no additional usage identifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_EXISTING"></a><a id="ctl_find_existing"></a><dl>
<dt><b>CTL_FIND_EXISTING</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">PCCTL_CONTEXT</a>.

Searches for the next CRL that is an exact match of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CTL_FIND_SUBJECT"></a><a id="ctl_find_subject"></a><dl>
<dt><b>CTL_FIND_SUBJECT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_subject_para">CTL_FIND_SUBJECT_PARA</a>.

A CTL having the specified subject is found. <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinctl">CertFindSubjectInCTL</a> can be called to get a pointer to the subject's entry in the CTL. The <b>pUsagePara</b> member in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_subject_para">CTL_FIND_SUBJECT_PARA</a> can optionally be set to enable the matching described preceding under CTL_FIND_USAGE.

</td>
</tr>
</table>

### -param pvFindPara [in]

A pointer to the search value associated with the <i>dwFindType</i> parameter.

### -param pPrevCtlContext [in]

A pointer to the last 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> returned by this function. It must be <b>NULL</b> to get the first CTL in the store. Successive CTLs are retrieved by setting <i>pPrevCtlContext</i> to the pointer to the <b>CTL_CONTEXT</b> returned by a previous function call. Any certificates that do not meet the search criteria or that have been previously deleted by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a> are skipped. This function frees the <b>CTL_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter.

## -returns

If the function succeeds, the return value is a pointer to a read-only <a href="/windows/desktop/SecGloss/c-gly">CTL</a><a href="/windows/desktop/SecGloss/c-gly">context</a>.

For extended error information, call 
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
Either no CTLs were found in the store, no CTL was found matching the search criteria, or the function reached the end of the store's list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the CTL context pointed to by the <i>pPrevCtlContext</i> parameter, or a value that is not valid was specified in the <i>dwFindType</i> parameter.

</td>
</tr>
</table>

## -remarks

A returned pointer is freed when passed as the <i>pPrevCtlContext</i> on a subsequent call to the function. Otherwise, the pointer must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>. A non-<b>NULL</b><i>pPrevCtlContext</i> passed to the function is always freed with a call to <b>CertFreeCTLContext</b>, even if the function generates an error.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a> can be called to make a duplicate of the returned context. The returned CTL context can be added to a different certificate store using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctlcontexttostore">CertAddCTLContextToStore</a>, or a link to that CTL context can be added to a noncollection store using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctllinktostore">CertAddCTLLinkToStore</a>. If a CTL matching the search criteria is not found, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctlcontexttostore">CertAddCTLContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctllinktostore">CertAddCTLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumctlsinstore">CertEnumCTLsInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinctl">CertFindSubjectInCTL</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>