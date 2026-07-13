---
UID: NF:wincrypt.CryptVerifyTimeStampSignature
title: CryptVerifyTimeStampSignature function (wincrypt.h)
description: Validates the time stamp signature on a specified array of bytes.
helpviewer_keywords: ["CryptVerifyTimeStampSignature","CryptVerifyTimeStampSignature function [Security]","security.cryptverifytimestampsignature","wincrypt/CryptVerifyTimeStampSignature"]
old-location: security\cryptverifytimestampsignature.htm
tech.root: security
ms.assetid: 791b1500-98e3-49d5-97aa-be91f5edb7c2
ms.date: 12/05/2018
ms.keywords: CryptVerifyTimeStampSignature, CryptVerifyTimeStampSignature function [Security], security.cryptverifytimestampsignature, wincrypt/CryptVerifyTimeStampSignature
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
 - CryptVerifyTimeStampSignature
 - wincrypt/CryptVerifyTimeStampSignature
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
 - CryptVerifyTimeStampSignature
---

# CryptVerifyTimeStampSignature function


## -description

The <b>CryptVerifyTimeStampSignature</b> function validates the time stamp signature on a specified array of bytes.

## -parameters

### -param pbTSContentInfo [in]

A pointer to a buffer that contains time stamp content.

### -param cbTSContentInfo

The size, in bytes, of the buffer pointed to by the <i>pbTSContentInfo</i> parameter.

### -param pbData [in, optional]

A pointer to an array of bytes on which to validate the time stamp signature.

### -param cbData

The size, in bytes, of the array pointed to by the <i>pbData</i> parameter.

### -param hAdditionalStore [in, optional]

The handle of an additional store to search for supporting
Time Stamping Authority (TSA) signing certificates and <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs).
    This parameter can be <b>NULL</b> if no additional store is to be searched.

### -param ppTsContext [out]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_context">PCRYPT_TIMESTAMP_CONTEXT</a> structure. When you have finished using the context, you must free it by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

### -param ppTsSigner [out, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCERT_CONTEXT</a> that
receives the certificate of the signer.
     When you have finished using this structure, you must free it by passing this
pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

Set this parameter to <b>NULL</b> if the TSA signer's certificate is not needed.

### -param phStore [out, optional]

A pointer to a handle that receives the certificate store opened  on CMS to search for supporting certificates.

This parameter can be <b>NULL</b> if the TSA supporting certificates are not needed. When you have finished using this handle,  you  must release it by passing it to  the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

## -returns

If the function succeeds, the function returns <b>TRUE</b>. For extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The caller should validate the <b>pszTSAPolicyId</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_timestamp_info">CRYPT_TIMESTAMP_INFO</a> structure when it is returned by the   <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrievetimestamp">CryptRetrieveTimeStamp</a> function. If a TSA policy was specified in the request 
     and the <b>ftTime</b> member contains a valid value, the caller should build a certificate context chain with which to populate the <i>ppTsSigner</i> parameter and validate the trust.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrievetimestamp">CryptRetrieveTimeStamp</a>