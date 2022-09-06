---
UID: NE:certenroll.X509CertificateTemplatePrivateKeyFlag
title: X509CertificateTemplatePrivateKeyFlag (certenroll.h)
description: Contains values that specify client actions regarding a private key.
helpviewer_keywords: ["PrivateKeyExportable","PrivateKeyRequireAlternateSignatureAlgorithm","PrivateKeyRequireArchival","PrivateKeyRequireStrongKeyProtection","X509CertificateTemplatePrivateKeyFlag","X509CertificateTemplatePrivateKeyFlag enumeration [Security]","certenroll/PrivateKeyExportable","certenroll/PrivateKeyRequireAlternateSignatureAlgorithm","certenroll/PrivateKeyRequireArchival","certenroll/PrivateKeyRequireStrongKeyProtection","certenroll/X509CertificateTemplatePrivateKeyFlag","security.x509certificatetemplateprivatekeyflag"]
old-location: security\x509certificatetemplateprivatekeyflag.htm
tech.root: security
ms.assetid: b908b5fb-9089-493d-9ef4-1fe429ec43d4
ms.date: 12/05/2018
ms.keywords: PrivateKeyExportable, PrivateKeyRequireAlternateSignatureAlgorithm, PrivateKeyRequireArchival, PrivateKeyRequireStrongKeyProtection, X509CertificateTemplatePrivateKeyFlag, X509CertificateTemplatePrivateKeyFlag enumeration [Security], certenroll/PrivateKeyExportable, certenroll/PrivateKeyRequireAlternateSignatureAlgorithm, certenroll/PrivateKeyRequireArchival, certenroll/PrivateKeyRequireStrongKeyProtection, certenroll/X509CertificateTemplatePrivateKeyFlag, security.x509certificatetemplateprivatekeyflag
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: X509CertificateTemplatePrivateKeyFlag
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509CertificateTemplatePrivateKeyFlag
 - certenroll/X509CertificateTemplatePrivateKeyFlag
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
 - X509CertificateTemplatePrivateKeyFlag
---

# X509CertificateTemplatePrivateKeyFlag enumeration


## -description

The <b>X509CertificateTemplatePrivateKeyFlag</b> enumeration contains values that specify client actions regarding a private key.

## -enum-fields

### -field PrivateKeyRequireArchival:0x1

Instructs the client to create a key archival certificate request.

### -field PrivateKeyExportable:0x10

Instructs the client to allow other applications to export the private key to a Personal Information Exchange (PFX) message. The message is typically saved in a file with a .pfx extension.

### -field PrivateKeyRequireStrongKeyProtection:0x20

Instructs the client to use additional protection for the private key.

### -field PrivateKeyRequireAlternateSignatureAlgorithm:0x40

If this flag is defined, the client must sign the certificate request by using the PKCS #1 version 2.1 signature format which requires that the hash algorithm OID be encoded into the signature parameters. If this flag is not defined the client must sign the certificate request by using the PKCS #1 version 1.5 signature format which requires that the hash and asymmetric algorithm object identifiers (OIDs) be combined into a single OID and that the signature parameters be set to <b>NULL</b>.

### -field PrivateKeyRequireSameKeyRenewal:0x80

### -field PrivateKeyUseLegacyProvider:0x100

### -field PrivateKeyEKTrustOnUse:0x200

### -field PrivateKeyEKValidateCert:0x400

### -field PrivateKeyEKValidateKey:0x800

### -field PrivateKeyAttestNone:0

### -field PrivateKeyAttestPreferred:0x1000

### -field PrivateKeyAttestRequired:0x2000

### -field PrivateKeyAttestMask:0x3000

### -field PrivateKeyAttestWithoutPolicy:0x4000

### -field PrivateKeyServerVersionMask:0xf0000

### -field PrivateKeyServerVersionShift:16

### -field PrivateKeyHelloKspKey:0x100000

### -field PrivateKeyHelloLogonKey:0x200000

### -field PrivateKeyClientVersionMask:0xf000000

### -field PrivateKeyClientVersionShift:24

