---
UID: NF:certenroll.ICertificateAttestationChallenge.DecryptChallenge
title: ICertificateAttestationChallenge::DecryptChallenge (certenroll.h)
author: windows-sdk-content
description: Decrypts the challenge from the Certificate Management over CMS (CMC) response and creates a re-encrypted response to send to the CA.
old-location: security\icertificateattestationchallenge_decryptchallenge.htm
tech.root: seccertenroll
ms.assetid: ae0fb86f-c567-4b85-abfe-7a035491e4fc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DecryptChallenge, DecryptChallenge method [Security], DecryptChallenge method [Security],ICertificateAttestationChallenge interface, ICertificateAttestationChallenge interface [Security],DecryptChallenge method, ICertificateAttestationChallenge.DecryptChallenge, ICertificateAttestationChallenge::DecryptChallenge, certenroll/ICertificateAttestationChallenge::DecryptChallenge, security.icertificateattestationchallenge_decryptchallenge
ms.topic: method
f1_keywords: 
 - "certenroll/ICertificateAttestationChallenge.DecryptChallenge"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - ICertificateAttestationChallenge.DecryptChallenge
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertificateAttestationChallenge::DecryptChallenge


## -description


Decrypts the challenge from the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response and creates a re-encrypted response to send to the CA.


## -parameters




### -param Encoding [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  attestation challenge. The default value is XCN_CRYPT_STRING_BASE64.


### -param pstrEnvelopedPkcs7ReencryptedToCA [out, retval]

The decrypted challenge from the CMC response re-encrypted for the CA.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificateattestationchallenge">ICertificateAttestationChallenge</a>
 

 

