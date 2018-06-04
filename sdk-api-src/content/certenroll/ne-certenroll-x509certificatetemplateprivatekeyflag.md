---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



