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

# _MFNetCredentialOptions enumeration


## -description



Describes options for the caching network credentials.




## -enum-fields




### -field MFNET_CREDENTIAL_SAVE

Allow the credential cache object to save  credentials in persistant storage.


### -field MFNET_CREDENTIAL_DONT_CACHE

Do not allow the credential cache object to cache the credentials in memory. This flag cannot be combined with the MFNET_CREDENTIAL_SAVE flag.


### -field MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT

The user allows credentials to be sent over the network in clear text.

 By default, <a href="https://msdn.microsoft.com/7e095445-354a-4fbb-b354-bf87eb77552f">IMFNetCredentialCache::GetCredential</a> always returns the REQUIRE_PROMPT flag when the authentication flags include MFNET_AUTHENTICATION_CLEAR_TEXT, even if cached credentials are available. If you set the MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT option, the <b>GetCredential</b> method will not return  REQUIRE_PROMPT for clear text, if cached credentials are available.

Do not set this flag without notifying the user that credentials might be sent in clear text.


## -see-also




<a href="https://msdn.microsoft.com/024eea57-e7c8-495d-9959-ab37dd45873d">IMFNetCredentialCache::SetUserOptions</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

