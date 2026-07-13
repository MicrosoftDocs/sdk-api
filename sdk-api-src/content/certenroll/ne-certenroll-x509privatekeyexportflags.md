---
UID: NE:certenroll.X509PrivateKeyExportFlags
title: X509PrivateKeyExportFlags (certenroll.h)
description: Specifies the export policy for a private key.
helpviewer_keywords: ["X509PrivateKeyExportFlags","X509PrivateKeyExportFlags enumeration [Security]","XCN_NCRYPT_ALLOW_ARCHIVING_FLAG","XCN_NCRYPT_ALLOW_EXPORT_FLAG","XCN_NCRYPT_ALLOW_EXPORT_NONE","XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG","XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG","certenroll/X509PrivateKeyExportFlags","certenroll/XCN_NCRYPT_ALLOW_ARCHIVING_FLAG","certenroll/XCN_NCRYPT_ALLOW_EXPORT_FLAG","certenroll/XCN_NCRYPT_ALLOW_EXPORT_NONE","certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG","certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG","security.x509privatekeyexportflags"]
old-location: security\x509privatekeyexportflags.htm
tech.root: security
ms.assetid: a50af298-a579-462f-8744-78aa84070360
ms.date: 12/05/2018
ms.keywords: X509PrivateKeyExportFlags, X509PrivateKeyExportFlags enumeration [Security], XCN_NCRYPT_ALLOW_ARCHIVING_FLAG, XCN_NCRYPT_ALLOW_EXPORT_FLAG, XCN_NCRYPT_ALLOW_EXPORT_NONE, XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG, XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG, certenroll/X509PrivateKeyExportFlags, certenroll/XCN_NCRYPT_ALLOW_ARCHIVING_FLAG, certenroll/XCN_NCRYPT_ALLOW_EXPORT_FLAG, certenroll/XCN_NCRYPT_ALLOW_EXPORT_NONE, certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG, certenroll/XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG, security.x509privatekeyexportflags
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
req.typenames: X509PrivateKeyExportFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509PrivateKeyExportFlags
 - certenroll/X509PrivateKeyExportFlags
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
 - X509PrivateKeyExportFlags
---

# X509PrivateKeyExportFlags enumeration


## -description

The <b>X509PrivateKeyExportFlags</b> enumeration type specifies the export policy for a <a href="/windows/desktop/SecGloss/p-gly">private key</a>. For a Cryptography API: Next Generation (CNG) key, the policy is stored by the key service provider (KSP), and it is the responsibility of the KSP to enforce the policy. When a  legacy <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) is specified, the policy is used when creating the key, and it is the responsibility of the CSP to enforce the policy. This enumeration is used when specifying and retrieving the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_exportpolicy">ExportPolicy</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a> interface.

## -enum-fields

### -field XCN_NCRYPT_ALLOW_EXPORT_NONE:0

Export is not allowed. This is the default value.

### -field XCN_NCRYPT_ALLOW_EXPORT_FLAG:0x1

The private key can be exported.

### -field XCN_NCRYPT_ALLOW_PLAINTEXT_EXPORT_FLAG:0x2

The private key can be exported in plaintext form.

### -field XCN_NCRYPT_ALLOW_ARCHIVING_FLAG:0x4

The private key can be exported once for archiving.

### -field XCN_NCRYPT_ALLOW_PLAINTEXT_ARCHIVING_FLAG:0x8

The private key can be exported once in plaintext form for archiving.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>
