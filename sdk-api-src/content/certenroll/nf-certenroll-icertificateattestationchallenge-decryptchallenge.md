---
UID: NF:certenroll.ICertificateAttestationChallenge.DecryptChallenge
title: ICertificateAttestationChallenge::DecryptChallenge
author: windows-sdk-content
description: Decrypts the challenge from the Certificate Management over CMS (CMC) response and creates a re-encrypted response to send to the CA.
old-location: security\icertificateattestationchallenge_decryptchallenge.htm
old-project: seccertenroll
ms.assetid: ae0fb86f-c567-4b85-abfe-7a035491e4fc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DecryptChallenge, DecryptChallenge method [Security], DecryptChallenge method [Security],ICertificateAttestationChallenge interface, ICertificateAttestationChallenge interface [Security],DecryptChallenge method, ICertificateAttestationChallenge.DecryptChallenge, ICertificateAttestationChallenge::DecryptChallenge, certenroll/ICertificateAttestationChallenge::DecryptChallenge, security.icertificateattestationchallenge_decryptchallenge
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - ICertificateAttestationChallenge.DecryptChallenge
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# ICertificateAttestationChallenge::DecryptChallenge


## -description


Decrypts the challenge from the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) response and creates a re-encrypted response to send to the CA.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  attestation challenge. The default value is XCN_CRYPT_STRING_BASE64.


### -param pstrEnvelopedPkcs7ReencryptedToCA [out, retval]

The decrypted challenge from the CMC response re-encrypted for the CA.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn379339(v=VS.85).aspx">ICertificateAttestationChallenge</a>
 

 

