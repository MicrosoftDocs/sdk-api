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

# _USERNAME_TARGET_CREDENTIAL_INFO structure


## -description


The 
<b>USERNAME_TARGET_CREDENTIAL_INFO</b> structure contains a reference to a credential. This structure is used to pass a user name into the 
<a href="https://msdn.microsoft.com/20a1d54b-04a7-4b0a-88e4-1970d1f71502">CredMarshalCredential</a> function and out of the 
<a href="https://msdn.microsoft.com/65757235-d92c-479f-8e2b-1f8d8564792b">CredUnmarshalCredential</a>. The resultant marshaled credential can be passed as the <i>lpszUserName</i> parameter of the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function to direct that API to get the password from the corresponding CRED_FLAGS_USERNAME_TARGET credential instead of from the <i>lpszPassword</i> parameter of the function.


## -struct-fields




### -field UserName

 User name of the USERNAME_TARGET_CREDENTIAL_INFO credential.

