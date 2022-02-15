---
UID: NE:certenroll.X509PrivateKeyUsageFlags
title: X509PrivateKeyUsageFlags (certenroll.h)
description: Specifies the permitted uses of a private key.
helpviewer_keywords: ["X509PrivateKeyUsageFlags","X509PrivateKeyUsageFlags enumeration [Security]","XCN_NCRYPT_ALLOW_ALL_USAGES","XCN_NCRYPT_ALLOW_DECRYPT_FLAG","XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG","XCN_NCRYPT_ALLOW_SIGNING_FLAG","XCN_NCRYPT_ALLOW_USAGES_NONE","certenroll/X509PrivateKeyUsageFlags","certenroll/XCN_NCRYPT_ALLOW_ALL_USAGES","certenroll/XCN_NCRYPT_ALLOW_DECRYPT_FLAG","certenroll/XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG","certenroll/XCN_NCRYPT_ALLOW_SIGNING_FLAG","certenroll/XCN_NCRYPT_ALLOW_USAGES_NONE","security.x509privatekeyusageflags"]
old-location: security\x509privatekeyusageflags.htm
tech.root: security
ms.assetid: 831c4c07-dc26-420a-ac04-d96248f3fad2
ms.date: 12/05/2018
ms.keywords: X509PrivateKeyUsageFlags, X509PrivateKeyUsageFlags enumeration [Security], XCN_NCRYPT_ALLOW_ALL_USAGES, XCN_NCRYPT_ALLOW_DECRYPT_FLAG, XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG, XCN_NCRYPT_ALLOW_SIGNING_FLAG, XCN_NCRYPT_ALLOW_USAGES_NONE, certenroll/X509PrivateKeyUsageFlags, certenroll/XCN_NCRYPT_ALLOW_ALL_USAGES, certenroll/XCN_NCRYPT_ALLOW_DECRYPT_FLAG, certenroll/XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG, certenroll/XCN_NCRYPT_ALLOW_SIGNING_FLAG, certenroll/XCN_NCRYPT_ALLOW_USAGES_NONE, security.x509privatekeyusageflags
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
req.typenames: X509PrivateKeyUsageFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509PrivateKeyUsageFlags
 - certenroll/X509PrivateKeyUsageFlags
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
 - X509PrivateKeyUsageFlags
---

# X509PrivateKeyUsageFlags enumeration


## -description

The <b>X509PrivateKeyUsageFlags</b> enumeration specifies the permitted uses of a <a href="/windows/desktop/SecGloss/p-gly">private key</a>. It is the responsibility of the cryptographic provider. The enumeration value can be set and retrieved by using the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyusage">KeyUsage</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface.

## -enum-fields

### -field XCN_NCRYPT_ALLOW_USAGES_NONE:0

The permitted uses are not defined.

### -field XCN_NCRYPT_ALLOW_DECRYPT_FLAG:0x1

The key can be used to decrypt content. This maps to the following <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyusageflags">X509KeyUsageFlags</a> values:

<ul>
<li>XCN_CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>XCN_CERT_DECIPHER_ONLY_KEY_USAGE</li>
<li>XCN_CERT_ENCIPHER_ONLY_KEY_USAGE</li>
<li>XCN_CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
</ul>

### -field XCN_NCRYPT_ALLOW_SIGNING_FLAG:0x2

The key can be used for signing. This maps to the following <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyusageflags">X509KeyUsageFlags</a> values:

<ul>
<li>XCN_CERT_CRL_SIGN_KEY_USAGE</li>
<li>XCN_CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>XCN_CERT_KEY_CERT_SIGN_KEY_USAGE</li>
</ul>

### -field XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG:0x4

The key can be used to establish key agreement between entities.

### -field XCN_NCRYPT_ALLOW_KEY_IMPORT_FLAG:0x8

### -field XCN_NCRYPT_ALLOW_ALL_USAGES:0xffffff

All of the uses defined for this enumeration are permitted.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
