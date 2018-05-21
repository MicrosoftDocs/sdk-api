---
UID: NS:eaptypes._EapCredential
title: "_EapCredential"
author: windows-driver-content
description: Contains information about the credentials type and the appropriate credentials. This is passed as an input to the EapPeerGetConfigBlobAndUserBlob API.
old-location: eaphost\eapcredential.htm
old-project: EAPHost
ms.assetid: DC1B9524-2853-404D-A77A-61CB012FCF11
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: EapCredential, EapCredential structure [EAPHost], _EapCredential, eaphost.eapcredential, eaptypes/EapCredential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: EapCredential
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	eaptypes.h
api_name:
-	EapCredential
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EapCredential structure


## -description


The <b>EapCredential</b> structure contains information about the credentials type and the appropriate credentials. This is passed as an input to the <a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a> API.


## -struct-fields




### -field credType

The <a href="https://msdn.microsoft.com/E77AA5E1-970A-43A6-916D-623A9C554F53">EapCredentialType</a> for the  credentials passed in the <i>credentials</i> parameter.


### -field credData.switch_is

 


### -field credData.switch_is.credType

 


### -field credData

Structure that holds the pointer to the credential data. 

If <b>credType</b> is set to <b>EAP_EMPTY_CREDENTIAL</b>, specify a NULL value for credentials.

If <b>credType</b> is set to  <b>EAP_USERNAME_PASSWORD_CREDENTIAL</b>, use an <a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a> structure to specify the username and password to use for the credentials. 

If <b>credType</b> is set to <b>EAP_WINLOGON_CREDENTIAL</b>, specify a NULL value for credentials. 

If <b>credType</b> is set to <b>EAP_CERTIFICATE_CREDENTIAL</b>, use an <a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a> structure for credentials to specify  the certificate hash and a password (in case the certificate is password protected). 

If <b>credType</b> is set to <b>EAP_SIM_CREDENTIAL</b>, use an <a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a> structure for credentials to specify the  ICC-ID of the selected SIM.


## -see-also




<a href="https://msdn.microsoft.com/575967F4-E5CC-433D-919D-258B5849A5B1">EapCertificateCredential</a>



<a href="https://msdn.microsoft.com/E77AA5E1-970A-43A6-916D-623A9C554F53">EapCredentialType</a>



<a href="https://msdn.microsoft.com/81817FAA-20AE-4556-BAA5-0EF2A955B6A3">EapPeerGetConfigBlobAndUserBlob</a>



<a href="https://msdn.microsoft.com/483BF257-BB9F-4AF6-A55C-77277AC6E21F">EapSimCredential</a>



<a href="https://msdn.microsoft.com/61484095-4354-4103-9E21-683002750B26">EapUsernamePasswordCredential</a>
 

 

