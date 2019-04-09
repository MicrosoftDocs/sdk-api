---
UID: NS:eaptypes._EapUsernamePasswordCredential
title: EapUsernamePasswordCredential (eaptypes.h)
author: windows-sdk-content
description: Contains the username and password that is used by the EAP method for authenticating the user.
old-location: eaphost\eapusernamepasswordcredential.htm
tech.root: eaphost
ms.assetid: 61484095-4354-4103-9E21-683002750B26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapUsernamePasswordCredential, EapUsernamePasswordCredential structure [EAPHost], eaphost.eapusernamepasswordcredential, eaptypes/EapUsernamePasswordCredential
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
 - EapUsernamePasswordCredential
product: Windows
targetos: Windows
req.typenames: EapUsernamePasswordCredential
req.redist: 
---

# EapUsernamePasswordCredential structure


## -description


The <b>EapUsernamePasswordCredential</b> structure contains the username and password that is used by the EAP method for authenticating the user.


## -struct-fields




### -field username

A NULL-terminated Unicode string that contains the username that needs authentication. The username uses the format user@domain or domain\user.


### -field password

A NULL-terminated Unicode string that contains the password to verify the user. The password is encrypted using the <a href="EapUsernamePasswordCredential ">CredProtect</a> function. The EAP method must use the <a href="https://msdn.microsoft.com/7a22fb2b-edfc-45f2-b2d2-729f3761584d">CredUnprotect</a> function to retrieve the unencrypted password.


## -see-also




<a href="https://msdn.microsoft.com/DC1B9524-2853-404D-A77A-61CB012FCF11">EapCredential</a>



<a href="https://msdn.microsoft.com/E77AA5E1-970A-43A6-916D-623A9C554F53">EapCredentialType</a>
 

 

