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

# _EapUsernamePasswordCredential structure


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
 

 

