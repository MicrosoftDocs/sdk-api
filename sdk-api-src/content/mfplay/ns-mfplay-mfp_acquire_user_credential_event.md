---
UID: NS:mfplay.MFP_ACQUIRE_USER_CREDENTIAL_EVENT
title: MFP_ACQUIRE_USER_CREDENTIAL_EVENT
author: windows-sdk-content
description: Event structure for the MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL event.
old-location: mf\mfp_acquire_user_credential_event.htm
tech.root: medfound
ms.assetid: 61767b81-8641-43d5-b272-148d52517727
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MFP_ACQUIRE_USER_CREDENTIAL_EVENT, MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure [Media Foundation], mf.mfp_acquire_user_credential_event, mfplay/MFP_ACQUIRE_USER_CREDENTIAL_EVENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_ACQUIRE_USER_CREDENTIAL_EVENT
product: Windows
targetos: Windows
req.typenames: MFP_ACQUIRE_USER_CREDENTIAL_EVENT
req.redist: 
---

# MFP_ACQUIRE_USER_CREDENTIAL_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL</b> event. This event is sent if the application plays a media file from a server that requires authentication. The application can respond by providing the user credentials.


## -struct-fields




### -field header


<a href="https://msdn.microsoft.com/ed9d3790-845a-4392-b755-6a5ce6e20de5">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> events.


### -field dwUserData

Application-defined user data for the media item. This value is specified when the application calls <a href="https://msdn.microsoft.com/7dc2a7f3-81b4-46c6-b45e-44c6a20afc6b">IMFPMediaPlayer::CreateMediaItemFromURL</a> or <a href="https://msdn.microsoft.com/d647df89-b874-448e-ae41-ee3bcb55521f">IMFPMediaPlayer::CreateMediaItemFromObject</a> to create the media item.

This event is sent (if at all) before the media item is created and before the application receives the <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b> event. You can use the value of <b>dwUserData</b> to identify which media item requires authentication.


### -field fProceedWithAuthentication

The application should set this member to either <b>TRUE</b> or <b>FALSE</b> before returning from the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> event callback. 

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

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/5aa13072-239a-41b6-a0b6-a2729bab2db4">_MFP_CREDENTIAL_FLAGS</a> enumeration.


### -field pCredential

Pointer to the <a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a> interface. The application uses this interface to set the user's credentials.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://msdn.microsoft.com/2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  callback method.  You can use the <a href="https://msdn.microsoft.com/4079acb8-8ae2-46e3-b7d9-50a700696fd6">MFP_GET_ACQUIRE_USER_CREDENTIAL_EVENT</a> macro for this purpose.

If the <b>flags</b> member contains the <b>MFP_CREDENTIAL_PROMPT</b> flag, the application should do the following:

<ol>
<li>Prompt the user to enter a user name and password.</li>
<li>Store the user name in the credentials object by calling <a href="https://msdn.microsoft.com/026a822a-4e48-4fc8-9781-5e427528a4d2">IMFNetCredential::SetUser</a> on the <b>pCredential</b> pointer.</li>
<li>Store the password by calling <a href="https://msdn.microsoft.com/7de58b57-83fe-4c3a-9029-e9be556c84c9">IMFNetCredential::SetPassword</a> on the <b>pCredential</b> pointer.</li>
</ol>
To cancel authentication, set <b>fProceedWithAuthentication</b> equal to <b>FALSE</b>.

By default, MFPlay uses the network source's implementation of <a href="https://msdn.microsoft.com/002d8608-4ef9-40fd-8dcc-fe6ade34478e">IMFNetCredentialManager</a> to manage credentials. An application can provide its own implementation of this interface as follows:

<ol>
<li>Call <b>QueryInterface</b> on the <a href="https://msdn.microsoft.com/fa57d465-1ee9-4f7a-9be8-66a6d73f65e8">IMFPMediaPlayer</a> pointer to get the <b>IPropertyStore</b> interface.</li>
<li>Call <b>IPropertyStore::SetValue</b> to set the <a href="https://msdn.microsoft.com/c0826956-9df1-40ec-8ad1-9e0dca34d847">MFNETSOURCE_CREDENTIAL_MANAGER</a> property.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/7d9d01bf-861a-4c35-93b1-dbf85cbf0a32">IMFPMediaPlayerCallback</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/6f143c51-ec46-46d4-9a1e-b04fcc0d8bea">Using MFPlay for Audio/Video Playback</a>
 

 

