---
UID: NS:eaptypes._EapCredential
title: EapCredential (eaptypes.h)
description: Contains information about the credentials type and the appropriate credentials. This is passed as an input to the EapPeerGetConfigBlobAndUserBlob API.
helpviewer_keywords: ["EapCredential","EapCredential structure [EAPHost]","eaphost.eapcredential","eaptypes/EapCredential"]
old-location: eaphost\eapcredential.htm
tech.root: eaphost
ms.assetid: DC1B9524-2853-404D-A77A-61CB012FCF11
ms.date: 12/05/2018
ms.keywords: EapCredential, EapCredential structure [EAPHost], eaphost.eapcredential, eaptypes/EapCredential
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
req.typenames: EapCredential
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EapCredential
 - eaptypes/_EapCredential
 - EapCredential
 - eaptypes/EapCredential
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
 - EapCredential
---

# EapCredential structure


## -description

The <b>EapCredential</b> structure contains information about the credentials type and the appropriate credentials. This is passed as an input to the <a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob">EapPeerGetConfigBlobAndUserBlob</a> API.

## -struct-fields

### -field credType

The <a href="/windows/desktop/api/eaptypes/ne-eaptypes-eapcredentialtype">EapCredentialType</a> for the  credentials passed in the <i>credentials</i> parameter.



### -field credData

Structure that holds the pointer to the credential data. 

If <b>credType</b> is set to <b>EAP_EMPTY_CREDENTIAL</b>, specify a NULL value for credentials.

If <b>credType</b> is set to  <b>EAP_USERNAME_PASSWORD_CREDENTIAL</b>, use an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential">EapUsernamePasswordCredential</a> structure to specify the username and password to use for the credentials. 

If <b>credType</b> is set to <b>EAP_WINLOGON_CREDENTIAL</b>, specify a NULL value for credentials. 

If <b>credType</b> is set to <b>EAP_CERTIFICATE_CREDENTIAL</b>, use an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential">EapCertificateCredential</a> structure for credentials to specify  the certificate hash and a password (in case the certificate is password protected). 

If <b>credType</b> is set to <b>EAP_SIM_CREDENTIAL</b>, use an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential">EapSimCredential</a> structure for credentials to specify the  ICC-ID of the selected SIM.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential">EapCertificateCredential</a>



<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eapcredentialtype">EapCredentialType</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob">EapPeerGetConfigBlobAndUserBlob</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential">EapSimCredential</a>



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential">EapUsernamePasswordCredential</a>