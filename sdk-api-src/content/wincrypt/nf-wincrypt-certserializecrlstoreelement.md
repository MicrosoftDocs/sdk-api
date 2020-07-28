---
UID: NF:wincrypt.CertSerializeCRLStoreElement
title: CertSerializeCRLStoreElement function (wincrypt.h)
description: The CertSerializeCRLStoreElement function serializes an encoded certificate revocation list (CRL) context and the encoded representation of its properties.
helpviewer_keywords: ["CertSerializeCRLStoreElement","CertSerializeCRLStoreElement function [Security]","_crypto2_certserializecrlstoreelement","security.certserializecrlstoreelement","wincrypt/CertSerializeCRLStoreElement"]
old-location: security\certserializecrlstoreelement.htm
tech.root: security
ms.assetid: 4ab053cd-d3d4-483c-b0ff-b8de63d88707
ms.date: 12/05/2018
ms.keywords: CertSerializeCRLStoreElement, CertSerializeCRLStoreElement function [Security], _crypto2_certserializecrlstoreelement, security.certserializecrlstoreelement, wincrypt/CertSerializeCRLStoreElement
f1_keywords:
- wincrypt/CertSerializeCRLStoreElement
dev_langs:
- c++
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
- CertSerializeCRLStoreElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertSerializeCRLStoreElement function


## -description


The <b>CertSerializeCRLStoreElement</b> function serializes an encoded <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a> and the encoded representation of its properties. The result can be persisted to storage so that the CRL and properties can be retrieved at a later time.


## -parameters




### -param pCrlContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure being serialized.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pbElement [out]

A pointer to a buffer to receive the serialized output, including the encoded CRL, and possibly its properties. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.


### -param pcbElement [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the buffer pointed to by the <i>pbElement</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>
 

 

