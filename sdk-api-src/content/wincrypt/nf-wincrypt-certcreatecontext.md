---
UID: NF:wincrypt.CertCreateContext
title: CertCreateContext function (wincrypt.h)
description: Creates the specified context from the encoded bytes. The context created does not include any extended properties.
helpviewer_keywords: ["CERT_CREATE_CONTEXT_NOCOPY_FLAG","CERT_CREATE_CONTEXT_NO_ENTRY_FLAG","CERT_CREATE_CONTEXT_NO_HCRYPTMSG_FLAG","CERT_CREATE_CONTEXT_SORTED_FLAG","CERT_STORE_CERTIFICATE_CONTEXT","CERT_STORE_CRL_CONTEXT","CERT_STORE_CTL_CONTEXT","CertCreateContext","CertCreateContext function [Security]","_crypto2_certcreatecontext","security.certcreatecontext","wincrypt/CertCreateContext"]
old-location: security\certcreatecontext.htm
tech.root: security
ms.assetid: 0911054b-a47a-4046-b121-a236fc4b018b
ms.date: 12/05/2018
ms.keywords: CERT_CREATE_CONTEXT_NOCOPY_FLAG, CERT_CREATE_CONTEXT_NO_ENTRY_FLAG, CERT_CREATE_CONTEXT_NO_HCRYPTMSG_FLAG, CERT_CREATE_CONTEXT_SORTED_FLAG, CERT_STORE_CERTIFICATE_CONTEXT, CERT_STORE_CRL_CONTEXT, CERT_STORE_CTL_CONTEXT, CertCreateContext, CertCreateContext function [Security], _crypto2_certcreatecontext, security.certcreatecontext, wincrypt/CertCreateContext
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
 - CertCreateContext
 - wincrypt/CertCreateContext
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
 - CertCreateContext
---

# CertCreateContext function


## -description

The <b>CertCreateContext</b> function creates the specified context from the encoded bytes. The context created does not include any extended properties.

## -parameters

### -param dwContextType [in]

Specifies the contexts that can be created. For example, to create a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> <a href="/windows/desktop/SecGloss/c-gly">context</a>, set <i>dwContextType</i> to CERT_STORE_CERTIFICATE_CONTEXT.
						

Currently defined context type flags are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CERTIFICATE_CONTEXT"></a><a id="cert_store_certificate_context"></a><dl>
<dt><b>CERT_STORE_CERTIFICATE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Certificate context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CRL_CONTEXT"></a><a id="cert_store_crl_context"></a><dl>
<dt><b>CERT_STORE_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
CRL context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTL_CONTEXT"></a><a id="cert_store_ctl_context"></a><dl>
<dt><b>CERT_STORE_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
CTL context.

</td>
</tr>
</table>

### -param dwEncodingType [in]

Specifies the encoding type used. Currently, only X509_ASN_ENCODING and PKCS_7_ASN_ENCODING are being used; however, additional encoding types may be added in the future. For either current encoding type, use: 


X509_ASN_ENCODING | PKCS_7_ASN_ENCODING.

### -param pbEncoded [in]

A pointer to a buffer that contains the existing encoded context content to be copied.

### -param cbEncoded [in]

The size, in bytes, of the <i>pbEncoded</i> buffer.

### -param dwFlags [in]

The following flag values are defined and can be combined by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_CONTEXT_NOCOPY_FLAG"></a><a id="cert_create_context_nocopy_flag"></a><dl>
<dt><b>CERT_CREATE_CONTEXT_NOCOPY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The created context points directly to the content pointed to by <i>pbEncoded</i> instead of an allocated copy.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_CONTEXT_SORTED_FLAG"></a><a id="cert_create_context_sorted_flag"></a><dl>
<dt><b>CERT_CREATE_CONTEXT_SORTED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The function creates a context with sorted entries. Currently, this flag only applies to a CTL context.

For CTLs, the <b>cCTLEntry</b> member of the returned 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> structure is always zero. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinsortedctl">CertFindSubjectInSortedCTL</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsubjectinsortedctl">CertEnumSubjectInSortedCTL</a> must be called to find or enumerate the CTL entries.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_CONTEXT_NO_HCRYPTMSG_FLAG"></a><a id="cert_create_context_no_hcryptmsg_flag"></a><dl>
<dt><b>CERT_CREATE_CONTEXT_NO_HCRYPTMSG_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, when a CTL context is created, a HCRYTPMSG handle to its <a href="/windows/desktop/SecCrypto/signeddata">SignedData</a> message is created. This flag can be set to improve performance by not creating this handle. This flag can only be used when <i>dwContextType</i> is CERT_STORE_CTL_CONTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_CONTEXT_NO_ENTRY_FLAG"></a><a id="cert_create_context_no_entry_flag"></a><dl>
<dt><b>CERT_CREATE_CONTEXT_NO_ENTRY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, when a CTL context is created, its entries are decoded. When this flag is set, the entries are not decoded and performance is improved. This flag can only be used when <i>dwContextType</i> is CERT_STORE_CTL_CONTEXT.

</td>
</tr>
</table>

### -param pCreatePara [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_create_context_para">CERT_CREATE_CONTEXT_PARA</a> structure. 




If <i>pCreatePara</i> and its <b>pfnFree</b> member are both non-<b>NULL</b>, the <b>pfnFree</b> member is used to free the memory specified by the <b>pvFree</b> member. If the <b>pvFree</b> member is <b>NULL</b>, the <b>pfnFree</b> member is used to free the <i>pbEncoded</i> pointer.

If <i>pCreatePara</i> or its <b>pfnFree</b> member is <b>NULL</b>, no attempt is made to free <i>pbEncoded</i>.

## -returns

If the function succeeds, the return value is a pointer to the newly created context. The <b>pvFree</b> member of <i>pCreatePara</i> must be called to free the created context.
						

If the function fails, the return value is <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_CANCELLED</b>, this means that the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func">PFN_CERT_CREATE_CONTEXT_SORT_FUNC</a> callback function returned <b>FALSE</b> to stop the sort.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumsubjectinsortedctl">CertEnumSubjectInSortedCTL</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinsortedctl">CertFindSubjectInSortedCTL</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate and Certificate Store Maintenance Functions</a>