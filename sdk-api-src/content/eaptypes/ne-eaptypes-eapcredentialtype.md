---
UID: NE:eaptypes._EapCredentialType
title: EapCredentialType (eaptypes.h)
description: Defines the set of possible EAP credentials that can be passed to the EapPeerGetConfigBlobAndUserBlob function.
helpviewer_keywords: ["EAP_CERTIFICATE_CREDENTIAL","EAP_EMPTY_CREDENTIAL","EAP_SIM_CREDENTIAL","EAP_USERNAME_PASSWORD_CREDENTIAL","EAP_WINLOGON_CREDENTIAL","EapCredentialType","EapCredentialType enumeration [EAPHost]","eaphost.eapcredentialtype","eaptypes/EAP_CERTIFICATE_CREDENTIAL","eaptypes/EAP_EMPTY_CREDENTIAL","eaptypes/EAP_SIM_CREDENTIAL","eaptypes/EAP_USERNAME_PASSWORD_CREDENTIAL","eaptypes/EAP_WINLOGON_CREDENTIAL","eaptypes/EapCredentialType"]
old-location: eaphost\eapcredentialtype.htm
tech.root: eaphost
ms.assetid: E77AA5E1-970A-43A6-916D-623A9C554F53
ms.date: 12/05/2018
ms.keywords: EAP_CERTIFICATE_CREDENTIAL, EAP_EMPTY_CREDENTIAL, EAP_SIM_CREDENTIAL, EAP_USERNAME_PASSWORD_CREDENTIAL, EAP_WINLOGON_CREDENTIAL, EapCredentialType, EapCredentialType enumeration [EAPHost], eaphost.eapcredentialtype, eaptypes/EAP_CERTIFICATE_CREDENTIAL, eaptypes/EAP_EMPTY_CREDENTIAL, eaptypes/EAP_SIM_CREDENTIAL, eaptypes/EAP_USERNAME_PASSWORD_CREDENTIAL, eaptypes/EAP_WINLOGON_CREDENTIAL, eaptypes/EapCredentialType
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
req.typenames: EapCredentialType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EapCredentialType
 - eaptypes/_EapCredentialType
 - EapCredentialType
 - eaptypes/EapCredentialType
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
 - EapCredentialType
---

# EapCredentialType enumeration


## -description

The <b>EapCredentialType</b> enumeration defines the set of possible EAP credentials that can be passed to the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob">EapPeerGetConfigBlobAndUserBlob</a> function.

## -enum-fields

### -field EAP_EMPTY_CREDENTIAL:0

The EAP method has no credential passed to it. The method must attempt a machine authentication.

### -field EAP_USERNAME_PASSWORD_CREDENTIAL

The EAP method uses a username and password for authentication. The credentials are passed using the <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential">EapUsernamePasswordCredential</a> structure.

### -field EAP_WINLOGON_CREDENTIAL

The EAP method uses the logged-on user credentials for authentication.

### -field EAP_CERTIFICATE_CREDENTIAL

The EAP method uses a certificate present on the system for authentication. The credential is passed as an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential">EapCertificateCredential</a> structure.

### -field EAP_SIM_CREDENTIAL

The EAP method uses a SIM for authentication. This is passed as an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential">EapSimCredential</a> structure.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential">EapCertificateCredential</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob">EapPeerGetConfigBlobAndUserBlob</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential">EapSimCredential</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential">EapUsernamePasswordCredential</a>
