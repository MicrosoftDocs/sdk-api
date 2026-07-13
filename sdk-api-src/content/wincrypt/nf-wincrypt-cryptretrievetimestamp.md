---
UID: NF:wincrypt.CryptRetrieveTimeStamp
title: CryptRetrieveTimeStamp function (wincrypt.h)
description: Encodes a time stamp request and retrieves the time stamp token from a location specified by a URL to a Time Stamping Authority (TSA).
helpviewer_keywords: ["CryptRetrieveTimeStamp","CryptRetrieveTimeStamp function [Security]","TIMESTAMP_DONT_HASH_DATA","TIMESTAMP_NO_AUTH_RETRIEVAL","TIMESTAMP_VERIFY_CONTEXT_SIGNATURE","security.cryptretrievetimestamp","wincrypt/CryptRetrieveTimeStamp"]
old-location: security\cryptretrievetimestamp.htm
tech.root: security
ms.assetid: 68ba3d40-08b0-4261-ab2f-6deb1795f830
ms.date: 12/05/2018
ms.keywords: CryptRetrieveTimeStamp, CryptRetrieveTimeStamp function [Security], TIMESTAMP_DONT_HASH_DATA, TIMESTAMP_NO_AUTH_RETRIEVAL, TIMESTAMP_VERIFY_CONTEXT_SIGNATURE, security.cryptretrievetimestamp, wincrypt/CryptRetrieveTimeStamp
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.Lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptRetrieveTimeStamp
 - wincrypt/CryptRetrieveTimeStamp
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
 - CryptRetrieveTimeStamp
---

# CryptRetrieveTimeStamp function


## -description

The <b>CryptRetrieveTimeStamp</b> function encodes a time stamp request and retrieves the time stamp token from a location specified by a URL to a Time Stamping Authority (TSA).

## -parameters

### -param wszUrl [in]

A pointer to a null-terminated wide character string that contains the URL of the TSA to which to send the request.

### -param dwRetrievalFlags

A set of flags that specify how the time stamp is retrieved.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_DONT_HASH_DATA"></a><a id="timestamp_dont_hash_data"></a><dl>
<dt><b>TIMESTAMP_DONT_HASH_DATA</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Inhibit hash calculation on the array of bytes pointed to by the <i>pbData</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_VERIFY_CONTEXT_SIGNATURE"></a><a id="timestamp_verify_context_signature"></a><dl>
<dt><b>TIMESTAMP_VERIFY_CONTEXT_SIGNATURE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Enforce signature validation on the retrieved time stamp.


<div class="alert"><b>Note</b>  The <b>TIMESTAMP_VERIFY_CONTEXT_SIGNATURE</b> flag is valid only      if the <b>fRequestCerts</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_para">CRYPT_TIMESTAMP_PARA</a> pointed to by the <i>pPara</i> parameter is set to <b>TRUE</b>.</div>
<div> </div>


</td>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_NO_AUTH_RETRIEVAL"></a><a id="timestamp_no_auth_retrieval"></a><dl>
<dt><b>TIMESTAMP_NO_AUTH_RETRIEVAL</b></dt>
<dt>0x00020000 </dt>
</dl>
</td>
<td width="60%">
Set this flag to inhibit automatic authentication handling.

</td>
</tr>
</table>

### -param dwTimeout

A <b>DWORD</b> value that specifies the maximum number of milliseconds to wait for retrieval. If this parameter is set to zero, this function does not time out.

### -param pszHashId [in]

A pointer to a null-terminated character string that contains the hash algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

### -param pPara [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_para">CRYPT_TIMESTAMP_PARA</a> structure that contains additional parameters for the request.

### -param pbData [in]

A pointer to an array of bytes to be time stamped.

### -param cbData

The size, in bytes, of the array pointed to by the <i>pbData</i> parameter.

### -param ppTsContext [out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_context">PCRYPT_TIMESTAMP_CONTEXT</a> structure. When you have finished using the context, you must free it by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

### -param ppTsSigner [out, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCERT_CONTEXT</a> that
receives the certificate of the signer.
     When you have finished using this structure, you must free it by passing this
pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.


Set this parameter to <b>NULL</b> if the TSA signer's certificate is not needed.

### -param phStore [out, optional]

The handle of a certificate store initialized with certificates from the time stamp response. This store can be used for validating the signer certificate of the time stamp response.

This parameter can be <b>NULL</b> if the TSA supporting certificates are not needed. When you have finished using this handle,  release it by passing it to  the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

## -returns

If the function is unable to retrieve, decode, and validate the time stamp context, it returns <b>FALSE</b>. For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifytimestampsignature">CryptVerifyTimeStampSignature</a>