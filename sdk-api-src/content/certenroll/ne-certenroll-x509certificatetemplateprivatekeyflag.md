---
UID: NE:certenroll.X509CertificateTemplatePrivateKeyFlag
title: X509CertificateTemplatePrivateKeyFlag
author: windows-sdk-content
description: Contains values that specify client actions regarding a private key.
old-location: security\x509certificatetemplateprivatekeyflag.htm
old-project: seccertenroll
ms.assetid: b908b5fb-9089-493d-9ef4-1fe429ec43d4
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PrivateKeyExportable, PrivateKeyRequireAlternateSignatureAlgorithm, PrivateKeyRequireArchival, PrivateKeyRequireStrongKeyProtection, X509CertificateTemplatePrivateKeyFlag, X509CertificateTemplatePrivateKeyFlag enumeration [Security], certenroll/PrivateKeyExportable, certenroll/PrivateKeyRequireAlternateSignatureAlgorithm, certenroll/PrivateKeyRequireArchival, certenroll/PrivateKeyRequireStrongKeyProtection, certenroll/X509CertificateTemplatePrivateKeyFlag, security.x509certificatetemplateprivatekeyflag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: X509CertificateTemplatePrivateKeyFlag
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509CertificateTemplatePrivateKeyFlag
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509CertificateTemplatePrivateKeyFlag enumeration


## -description


The <b>X509CertificateTemplatePrivateKeyFlag</b> enumeration contains values that specify client actions regarding a private key.


## -enum-fields




### -field PrivateKeyRequireArchival

Instructs the client to create a key archival certificate request.


### -field PrivateKeyExportable

Instructs the client to allow other applications to export the private key to a Personal Information Exchange (PFX) message. The message is typically saved in a file with a .pfx extension. 


### -field PrivateKeyRequireStrongKeyProtection

Instructs the client to use additional protection for the private key.


### -field PrivateKeyRequireAlternateSignatureAlgorithm

If this flag is defined, the client must sign the certificate request by using the PKCS #1 version 2.1 signature format which requires that the hash algorithm OID be encoded into the signature parameters. If this flag is not defined the client must sign the certificate request by using the PKCS #1 version 1.5 signature format which requires that the hash and asymmetric algorithm object identifiers (OIDs) be combined into a single OID and that the signature parameters be set to <b>NULL</b>.


### -field PrivateKeyRequireSameKeyRenewal


### -field PrivateKeyUseLegacyProvider


### -field PrivateKeyEKTrustOnUse


### -field PrivateKeyEKValidateCert


### -field PrivateKeyEKValidateKey


### -field PrivateKeyAttestNone


### -field PrivateKeyAttestPreferred


### -field PrivateKeyAttestRequired


### -field PrivateKeyAttestMask


### -field PrivateKeyAttestWithoutPolicy


### -field PrivateKeyServerVersionMask


### -field PrivateKeyServerVersionShift


### -field PrivateKeyHelloKspKey


### -field PrivateKeyHelloLogonKey


### -field PrivateKeyClientVersionMask


### -field PrivateKeyClientVersionShift



