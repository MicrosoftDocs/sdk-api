---
UID: NE:certenroll.X509KeyUsageFlags
title: X509KeyUsageFlags (certenroll.h)
description: Specifies the purpose of a key contained in a certificate.
helpviewer_keywords: ["X509KeyUsageFlags","X509KeyUsageFlags enumeration [Security]","XCN_CERT_CRL_SIGN_KEY_USAGE","XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE","XCN_CERT_DECIPHER_ONLY_KEY_USAGE","XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE","XCN_CERT_ENCIPHER_ONLY_KEY_USAGE","XCN_CERT_KEY_AGREEMENT_KEY_USAGE","XCN_CERT_KEY_CERT_SIGN_KEY_USAGE","XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE","XCN_CERT_NON_REPUDIATION_KEY_USAGE","XCN_CERT_NO_KEY_USAGE","XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE","certenroll/X509KeyUsageFlags","certenroll/XCN_CERT_CRL_SIGN_KEY_USAGE","certenroll/XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE","certenroll/XCN_CERT_DECIPHER_ONLY_KEY_USAGE","certenroll/XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE","certenroll/XCN_CERT_ENCIPHER_ONLY_KEY_USAGE","certenroll/XCN_CERT_KEY_AGREEMENT_KEY_USAGE","certenroll/XCN_CERT_KEY_CERT_SIGN_KEY_USAGE","certenroll/XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE","certenroll/XCN_CERT_NON_REPUDIATION_KEY_USAGE","certenroll/XCN_CERT_NO_KEY_USAGE","certenroll/XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE","security.x509keyusageflags_enum"]
old-location: security\x509keyusageflags_enum.htm
tech.root: security
ms.assetid: 3fcb91a3-ffcd-419f-a686-3fd2d1e795b3
ms.date: 12/05/2018
ms.keywords: X509KeyUsageFlags, X509KeyUsageFlags enumeration [Security], XCN_CERT_CRL_SIGN_KEY_USAGE, XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE, XCN_CERT_DECIPHER_ONLY_KEY_USAGE, XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE, XCN_CERT_ENCIPHER_ONLY_KEY_USAGE, XCN_CERT_KEY_AGREEMENT_KEY_USAGE, XCN_CERT_KEY_CERT_SIGN_KEY_USAGE, XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE, XCN_CERT_NON_REPUDIATION_KEY_USAGE, XCN_CERT_NO_KEY_USAGE, XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE, certenroll/X509KeyUsageFlags, certenroll/XCN_CERT_CRL_SIGN_KEY_USAGE, certenroll/XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE, certenroll/XCN_CERT_DECIPHER_ONLY_KEY_USAGE, certenroll/XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE, certenroll/XCN_CERT_ENCIPHER_ONLY_KEY_USAGE, certenroll/XCN_CERT_KEY_AGREEMENT_KEY_USAGE, certenroll/XCN_CERT_KEY_CERT_SIGN_KEY_USAGE, certenroll/XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE, certenroll/XCN_CERT_NON_REPUDIATION_KEY_USAGE, certenroll/XCN_CERT_NO_KEY_USAGE, certenroll/XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE, security.x509keyusageflags_enum
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
req.typenames: X509KeyUsageFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509KeyUsageFlags
 - certenroll/X509KeyUsageFlags
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
 - X509KeyUsageFlags
---

# X509KeyUsageFlags enumeration


## -description

The <b>X509KeyUsageFlags</b> enumeration type specifies the purpose of a key contained in a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. You can use the enumeration to identify restrictions. For example, if a key should be used only for signing, you can select the <b>XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE</b> or the <b>XCN_CERT_NON_REPUDIATION_KEY_USAGE</b> values. Likewise, if a key should be used only for key management, you can select the <b>XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE</b> value. This enumeration can be used to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a> object.

## -enum-fields

### -field XCN_CERT_NO_KEY_USAGE:0

The purpose of the key is not defined.

### -field XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE:0x80

The key is used with a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) to support services other than nonrepudiation, certificate signing, or revocation list signing.

### -field XCN_CERT_NON_REPUDIATION_KEY_USAGE:0x40

The key is used to verify a <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> as part of a nonrepudiation service that protects against false denial of action by a signing entity.

### -field XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE:0x20

The key is used for key transport. That is, the key is used to manage a key passed from its point of origination to another point of use.

### -field XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE:0x10

The key is used to encrypt user data other than cryptographic keys.

### -field XCN_CERT_KEY_AGREEMENT_KEY_USAGE:0x8

The key is used for key agreement. The key agreement or key exchange protocol enables two or more parties to negotiate a key value without transferring the key and without previously establishing a shared secret.

### -field XCN_CERT_KEY_CERT_SIGN_KEY_USAGE:0x4

The key is used to verify a certificate signature. This value can only be used for certificates issued by <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a>.

### -field XCN_CERT_OFFLINE_CRL_SIGN_KEY_USAGE:0x2

The key is used to verify an offline <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) signature.

### -field XCN_CERT_CRL_SIGN_KEY_USAGE:0x2

The key is used to verify a CRL signature.

### -field XCN_CERT_ENCIPHER_ONLY_KEY_USAGE:0x1

The key is used to encrypt data while performing key agreement. When this value is specified, the <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> value must also be specified.

### -field XCN_CERT_DECIPHER_ONLY_KEY_USAGE

The key is used to decrypt data while performing key agreement. When this value is specified, the <b>XCN_CERT_KEY_AGREEMENT_KEY_USAGE</b> must also be specified.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-initializeencode">InitializeEncode</a>
