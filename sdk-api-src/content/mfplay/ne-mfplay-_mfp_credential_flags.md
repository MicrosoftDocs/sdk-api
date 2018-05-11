---
UID: NE:mfplay._MFP_CREDENTIAL_FLAGS
title: "_MFP_CREDENTIAL_FLAGS"
author: windows-driver-content
description: Contains flags for the MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure.
old-location: mf\_mfp_credential_flags.htm
old-project: medfound
ms.assetid: 5aa13072-239a-41b6-a0b6-a2729bab2db4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MFP_CREDENTIAL_CLEAR_TEXT, MFP_CREDENTIAL_DO_NOT_CACHE, MFP_CREDENTIAL_LOGGED_ON_USER, MFP_CREDENTIAL_PROMPT, MFP_CREDENTIAL_PROXY, MFP_CREDENTIAL_SAVE, _MFP_CREDENTIAL_FLAGS, _MFP_CREDENTIAL_FLAGS enumeration [Media Foundation], mf._mfp_credential_flags, mfplay/MFP_CREDENTIAL_CLEAR_TEXT, mfplay/MFP_CREDENTIAL_DO_NOT_CACHE, mfplay/MFP_CREDENTIAL_LOGGED_ON_USER, mfplay/MFP_CREDENTIAL_PROMPT, mfplay/MFP_CREDENTIAL_PROXY, mfplay/MFP_CREDENTIAL_SAVE, mfplay/_MFP_CREDENTIAL_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfplay.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: "_MFP_CREDENTIAL_FLAGS"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfplay.h
api_name:
-	_MFP_CREDENTIAL_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

