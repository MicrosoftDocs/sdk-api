---
UID: NE:mfplay._MFP_CREDENTIAL_FLAGS
title: _MFP_CREDENTIAL_FLAGS (mfplay.h)
description: Contains flags for the MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure.
helpviewer_keywords: ["MFP_CREDENTIAL_CLEAR_TEXT","MFP_CREDENTIAL_DO_NOT_CACHE","MFP_CREDENTIAL_LOGGED_ON_USER","MFP_CREDENTIAL_PROMPT","MFP_CREDENTIAL_PROXY","MFP_CREDENTIAL_SAVE","_MFP_CREDENTIAL_FLAGS","_MFP_CREDENTIAL_FLAGS enumeration [Media Foundation]","mf._mfp_credential_flags","mfplay/MFP_CREDENTIAL_CLEAR_TEXT","mfplay/MFP_CREDENTIAL_DO_NOT_CACHE","mfplay/MFP_CREDENTIAL_LOGGED_ON_USER","mfplay/MFP_CREDENTIAL_PROMPT","mfplay/MFP_CREDENTIAL_PROXY","mfplay/MFP_CREDENTIAL_SAVE","mfplay/_MFP_CREDENTIAL_FLAGS"]
old-location: mf\_mfp_credential_flags.htm
tech.root: mf
ms.assetid: 5aa13072-239a-41b6-a0b6-a2729bab2db4
ms.date: 12/05/2018
ms.keywords: MFP_CREDENTIAL_CLEAR_TEXT, MFP_CREDENTIAL_DO_NOT_CACHE, MFP_CREDENTIAL_LOGGED_ON_USER, MFP_CREDENTIAL_PROMPT, MFP_CREDENTIAL_PROXY, MFP_CREDENTIAL_SAVE, _MFP_CREDENTIAL_FLAGS, _MFP_CREDENTIAL_FLAGS enumeration [Media Foundation], mf._mfp_credential_flags, mfplay/MFP_CREDENTIAL_CLEAR_TEXT, mfplay/MFP_CREDENTIAL_DO_NOT_CACHE, mfplay/MFP_CREDENTIAL_LOGGED_ON_USER, mfplay/MFP_CREDENTIAL_PROMPT, mfplay/MFP_CREDENTIAL_PROXY, mfplay/MFP_CREDENTIAL_SAVE, mfplay/_MFP_CREDENTIAL_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: _MFP_CREDENTIAL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFP_CREDENTIAL_FLAGS
 - mfplay/_MFP_CREDENTIAL_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - _MFP_CREDENTIAL_FLAGS
---

# _MFP_CREDENTIAL_FLAGS enumeration


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Contains flags for the <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_acquire_user_credential_event">MFP_ACQUIRE_USER_CREDENTIAL_EVENT</a> structure.

Some of these flags, marked [out], convey information back to the MFPlay player object. The application should set or clear these flags as appropriate, before returning from the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method.

## -enum-fields

### -field MFP_CREDENTIAL_PROMPT:0x1

The player object does not have any stored credentials and requires them from the application. If the player object can provide cached or stored credentials to the server, it does not set this flag.

### -field MFP_CREDENTIAL_SAVE:0x2

The credentials are saved to persistent storage. This flag acts as a hint for the application's UI. If the application prompts the user for credentials, the UI can indicate that the credentials have already been saved.



[out] If the application sets this flag, the player object saves the user credentials in persistent storage. Otherwise, the player object does not save the credentials.

### -field MFP_CREDENTIAL_DO_NOT_CACHE:0x4

[out] If the application sets this flag, the player object does not cache the user credentials in memory. Otherwise, the player object   does not cache the credentials. If you set this flag, do not set the <b>MFP_CREDENTIAL_SAVE</b> flag.

### -field MFP_CREDENTIAL_CLEAR_TEXT:0x8

The credentials will be sent in clear text. The application should  warn the user that the credentials will be sent over the network without encryption.

[out] On output, set this flag to allow the player object to send credentials in clear text, without prompting the user to re-enter the credentials.

### -field MFP_CREDENTIAL_PROXY:0x10

The credentials will be used to authenticate with a proxy.

### -field MFP_CREDENTIAL_LOGGED_ON_USER:0x20

The authentication scheme supports authentication of the user who is currently logged on.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
