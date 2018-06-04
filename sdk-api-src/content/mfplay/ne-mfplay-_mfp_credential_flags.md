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

# _MFP_CREDENTIAL_FLAGS enumeration


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Contains flags for the <a href="https://msdn.microsoft.com/61767b81-8641-43d5-b272-148d52517727">MFP_ACQUIRE_USER_CREDENTIAL_EVENT</a> structure.

Some of these flags, marked [out], convey information back to the MFPlay player object. The application should set or clear these flags as appropriate, before returning from the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method.


## -enum-fields




### -field MFP_CREDENTIAL_PROMPT

The player object does not have any stored credentials and requires them from the application. If the player object can provide cached or stored credentials to the server, it does not set this flag.


### -field MFP_CREDENTIAL_SAVE

The credentials are saved to persistent storage. This flag acts as a hint for the application's UI. If the application prompts the user for credentials, the UI can indicate that the credentials have already been saved.



[out] If the application sets this flag, the player object saves the user credentials in persistent storage. Otherwise, the player object does not save the credentials.


### -field MFP_CREDENTIAL_DO_NOT_CACHE


            [out] If the application sets this flag, the player object does not cache the user credentials in memory. Otherwise, the player object   does not cache the credentials. If you set this flag, do not set the <b>MFP_CREDENTIAL_SAVE</b> flag.
          


### -field MFP_CREDENTIAL_CLEAR_TEXT

The credentials will be sent in clear text. The application should  warn the user that the credentials will be sent over the network without encryption.

[out] On output, set this flag to allow the player object to send credentials in clear text, without prompting the user to re-enter the credentials.


### -field MFP_CREDENTIAL_PROXY

The credentials will be used to authenticate with a proxy.




### -field MFP_CREDENTIAL_LOGGED_ON_USER


            The authentication scheme supports authentication of the user who is currently logged on.
          


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

