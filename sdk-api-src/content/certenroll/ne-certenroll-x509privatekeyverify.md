---
UID: NE:certenroll.X509PrivateKeyVerify
title: X509PrivateKeyVerify (certenroll.h)
description: Specifies whether a user interface is displayed during private key verification and whether verification can proceed if the cryptographic provider is a smart card provider.
helpviewer_keywords: ["VerifyAllowUI","VerifyNone","VerifySilent","VerifySmartCardNone","VerifySmartCardSilent","X509PrivateKeyVerify","X509PrivateKeyVerify enumeration [Security]","certenroll/VerifyAllowUI","certenroll/VerifyNone","certenroll/VerifySilent","certenroll/VerifySmartCardNone","certenroll/VerifySmartCardSilent","certenroll/X509PrivateKeyVerify","security.x509privatekeyverify"]
old-location: security\x509privatekeyverify.htm
tech.root: security
ms.assetid: 23466035-6554-490f-ad46-e97ba5a5d996
ms.date: 12/05/2018
ms.keywords: VerifyAllowUI, VerifyNone, VerifySilent, VerifySmartCardNone, VerifySmartCardSilent, X509PrivateKeyVerify, X509PrivateKeyVerify enumeration [Security], certenroll/VerifyAllowUI, certenroll/VerifyNone, certenroll/VerifySilent, certenroll/VerifySmartCardNone, certenroll/VerifySmartCardSilent, certenroll/X509PrivateKeyVerify, security.x509privatekeyverify
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: X509PrivateKeyVerify
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509PrivateKeyVerify
 - certenroll/X509PrivateKeyVerify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509PrivateKeyVerify
---

# X509PrivateKeyVerify enumeration


## -description

The <b>X509PrivateKeyVerify</b> enumeration specifies whether a user interface is displayed during <a href="/windows/desktop/SecGloss/p-gly">private key</a> verification and whether verification can proceed if the cryptographic provider is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> provider. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-verify">Verify</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface.

## -enum-fields

### -field VerifyNone:0

No option is identified.

### -field VerifySilent:1

The method does not display a user interface.

### -field VerifySmartCardNone:2

No verification occurs if the key is stored on a smart card (the CSP or KSP is a smart card provider).

### -field VerifySmartCardSilent:3

The method does not display a user interface if the key is stored on a smart card (the CSP or KSP is a smart card provider).

### -field VerifyAllowUI:4

The method displays a user interface.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
