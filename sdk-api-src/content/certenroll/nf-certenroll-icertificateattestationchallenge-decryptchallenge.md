---
UID: NF:certenroll.ICertificateAttestationChallenge.DecryptChallenge
title: ICertificateAttestationChallenge::DecryptChallenge (certenroll.h)
description: Decrypts the challenge from the Certificate Management over CMS (CMC) response and creates a re-encrypted response to send to the CA.
helpviewer_keywords: ["DecryptChallenge","DecryptChallenge method [Security]","DecryptChallenge method [Security]","ICertificateAttestationChallenge interface","ICertificateAttestationChallenge interface [Security]","DecryptChallenge method","ICertificateAttestationChallenge.DecryptChallenge","ICertificateAttestationChallenge::DecryptChallenge","certenroll/ICertificateAttestationChallenge::DecryptChallenge","security.icertificateattestationchallenge_decryptchallenge"]
old-location: security\icertificateattestationchallenge_decryptchallenge.htm
tech.root: security
ms.assetid: ae0fb86f-c567-4b85-abfe-7a035491e4fc
ms.date: 12/05/2018
ms.keywords: DecryptChallenge, DecryptChallenge method [Security], DecryptChallenge method [Security],ICertificateAttestationChallenge interface, ICertificateAttestationChallenge interface [Security],DecryptChallenge method, ICertificateAttestationChallenge.DecryptChallenge, ICertificateAttestationChallenge::DecryptChallenge, certenroll/ICertificateAttestationChallenge::DecryptChallenge, security.icertificateattestationchallenge_decryptchallenge
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateAttestationChallenge::DecryptChallenge
 - certenroll/ICertificateAttestationChallenge::DecryptChallenge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - ICertificateAttestationChallenge.DecryptChallenge
---

# ICertificateAttestationChallenge::DecryptChallenge


## -description

Decrypts the challenge from the <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response and creates a re-encrypted response to send to the CA.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  attestation challenge. The default value is XCN_CRYPT_STRING_BASE64.

### -param pstrEnvelopedPkcs7ReencryptedToCA [out, retval]

The decrypted challenge from the CMC response re-encrypted for the CA.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificateattestationchallenge">ICertificateAttestationChallenge</a>