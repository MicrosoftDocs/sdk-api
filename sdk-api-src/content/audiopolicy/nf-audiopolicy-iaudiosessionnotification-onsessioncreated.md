---
UID: NF:audiopolicy.IAudioSessionNotification.OnSessionCreated
title: IAudioSessionNotification::OnSessionCreated (audiopolicy.h)
description: The OnSessionCreated method notifies the registered processes that the audio session has been created.
helpviewer_keywords: ["IAudioSessionNotification interface [Core Audio]","OnSessionCreated method","IAudioSessionNotification.OnSessionCreated","IAudioSessionNotification::OnSessionCreated","OnSessionCreated","OnSessionCreated method [Core Audio]","OnSessionCreated method [Core Audio]","IAudioSessionNotification interface","audiopolicy/IAudioSessionNotification::OnSessionCreated","coreaudio.iaudiosessionnotification_onsessioncreated"]
old-location: coreaudio\iaudiosessionnotification_onsessioncreated.htm
tech.root: CoreAudio
ms.assetid: 03f22e06-f446-4c57-a955-3d12deec4152
ms.date: 12/05/2018
ms.keywords: IAudioSessionNotification interface [Core Audio],OnSessionCreated method, IAudioSessionNotification.OnSessionCreated, IAudioSessionNotification::OnSessionCreated, OnSessionCreated, OnSessionCreated method [Core Audio], OnSessionCreated method [Core Audio],IAudioSessionNotification interface, audiopolicy/IAudioSessionNotification::OnSessionCreated, coreaudio.iaudiosessionnotification_onsessioncreated
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
 - IAudioSessionNotification::OnSessionCreated
 - audiopolicy/IAudioSessionNotification::OnSessionCreated
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
 - IAudioSessionNotification.OnSessionCreated
---

# IAudioSessionNotification::OnSessionCreated


## -description

The <b>OnSessionCreated</b> method notifies the registered processes that the audio session has been created.

## -parameters

### -param NewSession [in]

Pointer to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> interface of the audio session that was created.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

After registering its <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface, the application receives event notifications in the form of callbacks through the methods of the interface.

The audio engine calls <b>OnSessionCreated</b> when a new session is activated on the device endpoint.
This method is called from the session manager thread.  This method must take a reference to the session in the <i>NewSession</i> parameter if it wants to keep the reference after this call completes.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a>