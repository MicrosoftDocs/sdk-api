---
UID: NF:audiopolicy.IAudioSessionManager2.GetSessionEnumerator
title: IAudioSessionManager2::GetSessionEnumerator (audiopolicy.h)
description: The GetSessionEnumerator method gets a pointer to the audio session enumerator object.
helpviewer_keywords: ["GetSessionEnumerator","GetSessionEnumerator method [Core Audio]","GetSessionEnumerator method [Core Audio]","IAudioSessionManager2 interface","IAudioSessionManager2 interface [Core Audio]","GetSessionEnumerator method","IAudioSessionManager2.GetSessionEnumerator","IAudioSessionManager2::GetSessionEnumerator","audiopolicy/IAudioSessionManager2::GetSessionEnumerator","coreaudio.iaudiosessionmanager2_getsessionenumerator"]
old-location: coreaudio\iaudiosessionmanager2_getsessionenumerator.htm
tech.root: CoreAudio
ms.assetid: 68166fc1-af27-4251-8e18-be23d205b567
ms.date: 12/05/2018
ms.keywords: GetSessionEnumerator, GetSessionEnumerator method [Core Audio], GetSessionEnumerator method [Core Audio],IAudioSessionManager2 interface, IAudioSessionManager2 interface [Core Audio],GetSessionEnumerator method, IAudioSessionManager2.GetSessionEnumerator, IAudioSessionManager2::GetSessionEnumerator, audiopolicy/IAudioSessionManager2::GetSessionEnumerator, coreaudio.iaudiosessionmanager2_getsessionenumerator
req.header: audiopolicy.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSessionManager2::GetSessionEnumerator
 - audiopolicy/IAudioSessionManager2::GetSessionEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionManager2.GetSessionEnumerator
---

# IAudioSessionManager2::GetSessionEnumerator


## -description

The <b>GetSessionEnumerator</b> method gets a pointer to the audio session enumerator object.

## -parameters

### -param SessionEnum [out]

Receives a pointer to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator</a> interface of the session enumerator object that the client can use to enumerate audio sessions on the audio device. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

The session manager maintains a collection of audio sessions that are active on the audio device by querying the audio engine.  <b>GetSessionEnumerator</b>  creates a session control for each session in the collection. To get a reference to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> interface of the session in the enumerated collection, the application must call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessionidentifier">IAudioSessionEnumerator::GetSession</a>. For a code example, see <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator Interface</a>.

The session enumerator might not be aware of the new sessions that are reported through <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a>. So if an application exclusively relies on the session enumerator for getting all the sessions for an audio endpoint, the results might not be accurate. To work around this, the application should manually maintain a list. For more information, see <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a>