---
UID: NF:wincrypt.CertSerializeCertificateStoreElement
title: CertSerializeCertificateStoreElement function (wincrypt.h)
description: The CertSerializeCertificateStoreElement function serializes a certificate context's encoded certificate and its encoded properties. The result can be persisted to storage so that the certificate and properties can be retrieved at a later time.
helpviewer_keywords: ["CertSerializeCertificateStoreElement","CertSerializeCertificateStoreElement function [Security]","_crypto2_certserializecertificatestoreelement","security.certserializecertificatestoreelement","wincrypt/CertSerializeCertificateStoreElement"]
old-location: security\certserializecertificatestoreelement.htm
tech.root: security
ms.assetid: 104fc986-6344-41b7-8843-23c3c72405a2
ms.date: 12/05/2018
ms.keywords: CertSerializeCertificateStoreElement, CertSerializeCertificateStoreElement function [Security], _crypto2_certserializecertificatestoreelement, security.certserializecertificatestoreelement, wincrypt/CertSerializeCertificateStoreElement
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
 - CertSerializeCertificateStoreElement
 - wincrypt/CertSerializeCertificateStoreElement
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
 - CertSerializeCertificateStoreElement
---

# CertSerializeCertificateStoreElement function


## -description

The <b>CertSerializeCertificateStoreElement</b> function serializes a certificate context's encoded certificate and its encoded properties. The result can be persisted to storage so that the certificate and properties can be retrieved at a later time.

## -parameters

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> to be serialized.

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param pbElement [out]

A pointer to a buffer that receives the serialized output, including the encoded certificate and possibly its properties. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbElement [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the buffer pointed to by the <i>pbElement</i> parameter. When the function returns, <b>DWORD</b> value contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>