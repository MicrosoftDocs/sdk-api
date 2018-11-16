---
UID: NE:eaptypes._EapCredentialType
title: "_EapCredentialType"
author: windows-sdk-content
description: Defines the set of possible EAP credentials that can be passed to the EapPeerGetConfigBlobAndUserBlob function.
old-location: eaphost\eapcredentialtype.htm
tech.root: EAPHost
ms.assetid: E77AA5E1-970A-43A6-916D-623A9C554F53
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EAP_CERTIFICATE_CREDENTIAL, EAP_EMPTY_CREDENTIAL, EAP_SIM_CREDENTIAL, EAP_USERNAME_PASSWORD_CREDENTIAL, EAP_WINLOGON_CREDENTIAL, EapCredentialType, EapCredentialType enumeration [EAPHost], _EapCredentialType, eaphost.eapcredentialtype, eaptypes/EAP_CERTIFICATE_CREDENTIAL, eaptypes/EAP_EMPTY_CREDENTIAL, eaptypes/EAP_SIM_CREDENTIAL, eaptypes/EAP_USERNAME_PASSWORD_CREDENTIAL, eaptypes/EAP_WINLOGON_CREDENTIAL, eaptypes/EapCredentialType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EapCredentialType
product: Windows
targetos: Windows
req.typenames: EapCredentialType
req.redist: 
---

# _EapCredentialType enumeration


## -description


The <b>EapCredentialType</b> enumeration defines the set of possible EAP credentials that can be passed to the <a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a> function.


## -enum-fields




### -field EAP_EMPTY_CREDENTIAL

The EAP method has no credential passed to it. The method must attempt a machine authentication.


### -field EAP_USERNAME_PASSWORD_CREDENTIAL

The EAP method uses a username and password for authentication. The credentials are passed using the <a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a> structure.


### -field EAP_WINLOGON_CREDENTIAL

The EAP method uses the logged-on user credentials for authentication.


### -field EAP_CERTIFICATE_CREDENTIAL

The EAP method uses a certificate present on the system for authentication. The credential is passed as an <a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a> structure.


### -field EAP_SIM_CREDENTIAL

The EAP method uses a SIM for authentication. This is passed as an <a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a>



<a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a>



<a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a>



<a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a>
 

 

