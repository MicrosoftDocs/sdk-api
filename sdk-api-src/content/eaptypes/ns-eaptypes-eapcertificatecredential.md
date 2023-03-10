---
UID: NS:eaptypes._EapCertificateCredential
title: EapCertificateCredential (eaptypes.h)
description: Contains information about the certificate that the EAP method uses for authentication.
helpviewer_keywords: ["EapCertificateCredential","EapCertificateCredential structure [EAPHost]","eaphost.eapcertificatecredential","eaptypes/EapCertificateCredential"]
old-location: eaphost\eapcertificatecredential.htm
tech.root: eaphost
ms.assetid: 575967F4-E5CC-433D-919D-258B5849A5B1
ms.date: 12/05/2018
ms.keywords: EapCertificateCredential, EapCertificateCredential structure [EAPHost], eaphost.eapcertificatecredential, eaptypes/EapCertificateCredential
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: EapCertificateCredential
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EapCertificateCredential
 - eaptypes/_EapCertificateCredential
 - EapCertificateCredential
 - eaptypes/EapCertificateCredential
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EapCertificateCredential
---

## -description

The <b>EapCertificateCredential</b> structure contains information about the certificate that the EAP method uses for authentication.

## -struct-fields

### -field certHash

SHA1 hash of the certificate.

### -field password

If the certificate is present on the system and strong private key protection is turned on for this certificate, this field contains the password to access the certificate.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential">EapCredential</a>

<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eapcredentialtype">EapCredentialType</a>
