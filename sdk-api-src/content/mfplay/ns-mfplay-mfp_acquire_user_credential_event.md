---
UID: NS:mfplay.MFP_ACQUIRE_USER_CREDENTIAL_EVENT
title: MFP_ACQUIRE_USER_CREDENTIAL_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL event.
helpviewer_keywords: ["MFP_ACQUIRE_USER_CREDENTIAL_EVENT","MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure [Media Foundation]","mf.mfp_acquire_user_credential_event","mfplay/MFP_ACQUIRE_USER_CREDENTIAL_EVENT"]
old-location: mf\mfp_acquire_user_credential_event.htm
tech.root: mfarchive
archived: true
ms.assetid: 61767b81-8641-43d5-b272-148d52517727
ms.date: 12/05/2018
ms.keywords: MFP_ACQUIRE_USER_CREDENTIAL_EVENT, MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure [Media Foundation], mf.mfp_acquire_user_credential_event, mfplay/MFP_ACQUIRE_USER_CREDENTIAL_EVENT
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFP_ACQUIRE_USER_CREDENTIAL_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_ACQUIRE_USER_CREDENTIAL_EVENT
 - mfplay/MFP_ACQUIRE_USER_CREDENTIAL_EVENT
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
 - MFP_ACQUIRE_USER_CREDENTIAL_EVENT
---

# MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Event structure for the <b>MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL</b> event. This event is sent if the application plays a media file from a server that requires authentication. The application can respond by providing the user credentials.

## -struct-fields

### -field header

<a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.

### -field dwUserData

Application-defined user data for the media item. This value is specified when the application calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a> or <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create the media item.

This event is sent (if at all) before the media item is created and before the application receives the <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b> event. You can use the value of <b>dwUserData</b> to identify which media item requires authentication.

### -field fProceedWithAuthentication

The application should set this member to either <b>TRUE</b> or <b>FALSE</b> before returning from the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> event callback. 

If the value is <b>TRUE</b> when the callback returns, MFPlay continues the authentication attempt. Otherwise, authentication fails.

### -field hrAuthenticationStatus

The response code of the authentication challenge.

### -field pwszURL

The original URL that requires authentication.

### -field pwszSite

The name of the site or proxy that requires authentication.

### -field pwszRealm

The name of the realm for this authentication.

### -field pwszPackage

The name of the authentication package, such as "Digest" or "MBS_BASIC".

### -field nRetries

The number of retries. This member is set to zero on the first attempt, and incremented once for each subsequent attempt.

### -field flags

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/win32/api/mfplay/ne-mfplay-_mfp_credential_flags">_MFP_CREDENTIAL_FLAGS</a> enumeration.

### -field pCredential

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential">IMFNetCredential</a> interface. The application uses this interface to set the user's credentials.

## -remarks

To get a pointer to this structure, cast the <i>pEventHeader</i> parameter of the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  callback method.  You can use the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfp_get_acquire_user_credential_event">MFP_GET_ACQUIRE_USER_CREDENTIAL_EVENT</a> macro for this purpose.

If the <b>flags</b> member contains the <b>MFP_CREDENTIAL_PROMPT</b> flag, the application should do the following:

<ol>
<li>Prompt the user to enter a user name and password.</li>
<li>Store the user name in the credentials object by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser">IMFNetCredential::SetUser</a> on the <b>pCredential</b> pointer.</li>
<li>Store the password by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword">IMFNetCredential::SetPassword</a> on the <b>pCredential</b> pointer.</li>
</ol>
To cancel authentication, set <b>fProceedWithAuthentication</b> equal to <b>FALSE</b>.

By default, MFPlay uses the network source's implementation of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager">IMFNetCredentialManager</a> to manage credentials. An application can provide its own implementation of this interface as follows:

<ol>
<li>Call <b>QueryInterface</b> on the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> pointer to get the <b>IPropertyStore</b> interface.</li>
<li>Call <b>IPropertyStore::SetValue</b> to set the <a href="/windows/desktop/medfound/mfnetsource-credential-manager-property">MFNETSOURCE_CREDENTIAL_MANAGER</a> property.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>