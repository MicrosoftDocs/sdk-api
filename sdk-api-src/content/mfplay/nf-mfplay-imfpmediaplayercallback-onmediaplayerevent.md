---
UID: NF:mfplay.IMFPMediaPlayerCallback.OnMediaPlayerEvent
title: IMFPMediaPlayerCallback::OnMediaPlayerEvent (mfplay.h)
description: Called by the MFPlay player object to notify the application of a playback event.
helpviewer_keywords: ["IMFPMediaPlayerCallback interface [Media Foundation]","OnMediaPlayerEvent method","IMFPMediaPlayerCallback.OnMediaPlayerEvent","IMFPMediaPlayerCallback::OnMediaPlayerEvent","OnMediaPlayerEvent","OnMediaPlayerEvent method [Media Foundation]","OnMediaPlayerEvent method [Media Foundation]","IMFPMediaPlayerCallback interface","mf.imfpmediaplayercallback_onmediaplayerevent","mfplay/IMFPMediaPlayerCallback::OnMediaPlayerEvent"]
old-location: mf\imfpmediaplayercallback_onmediaplayerevent.htm
tech.root: mfarchive
archived: true
ms.assetid: 2a80a9d0-83ee-4bb0-ab2c-0f68367f3bf8
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayerCallback interface [Media Foundation],OnMediaPlayerEvent method, IMFPMediaPlayerCallback.OnMediaPlayerEvent, IMFPMediaPlayerCallback::OnMediaPlayerEvent, OnMediaPlayerEvent, OnMediaPlayerEvent method [Media Foundation], OnMediaPlayerEvent method [Media Foundation],IMFPMediaPlayerCallback interface, mf.imfpmediaplayercallback_onmediaplayerevent, mfplay/IMFPMediaPlayerCallback::OnMediaPlayerEvent
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMediaPlayerCallback::OnMediaPlayerEvent
 - mfplay/IMFPMediaPlayerCallback::OnMediaPlayerEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaPlayerCallback.OnMediaPlayerEvent
---

# IMFPMediaPlayerCallback::OnMediaPlayerEvent


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Called by the MFPlay player object to notify the application of a playback event.

## -parameters

### -param pEventHeader [in]

Pointer to an <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains information about the event.

## -remarks

The specific type of playback event is given in the <b>eEventType</b> member of the <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure. This structure contains information that is common to all of the event types. Some event types use extended structures. A set of macros is defined for casting the <i>pEventHeader</i> pointer to the correct structure type. For more information, see <a href="/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type">MFP_EVENT_TYPE</a>.
      

It is safe to call <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> and <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> methods inside the <b>OnMediaPlayer</b> method. MFPlay is guaranteed not to reenter the <b>OnMediaPlayer</b> method. That is, calls to <b>OnMediaPlayer</b> are serialized, and the method will not be invoked again from inside <b>OnMediaPlayer</b>. 


#### Examples

The following code shows how to cast the <i>pEventHeader</i> parameter to the correct structure type and pass the structure pointer to a handler function. The handler functions are declared at the start of the example. The application would need to provide implementations for these functions.  Note that you do not have to handle every event. For example, if your application never calls <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setrate">IMFPMediaPlayer::SetRate</a>, you would not need to handle the <b>MFP_EVENT_TYPE_RATE_SET</b> event. In that case, simply omit <b>MFP_EVENT_TYPE_RATE_SET</b> from the <b>switch</b> statement.


```cpp
// Declarations of MFPlay event handler functions.

void OnPlay(MFP_PLAY_EVENT *pEvent);
void OnPause(MFP_PAUSE_EVENT *pEvent);
void OnStop(MFP_STOP_EVENT *pEvent);
void OnPositionSet(MFP_POSITION_SET_EVENT *pEvent);
void OnRateSet(MFP_RATE_SET_EVENT *pEvent);
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent);
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT *pEvent);
void OnFrameStep(MFP_FRAME_STEP_EVENT *pEvent);
void OnMediaItemCleared(MFP_MEDIAITEM_CLEARED_EVENT *pEvent);
void OnMFEvent(MFP_MF_EVENT *pEvent); 
void OnError(MFP_ERROR_EVENT *pEvent);
void OnPlaybackEnded(MFP_PLAYBACK_ENDED_EVENT *pEvent);
void OnAquireUserCredential(MFP_ACQUIRE_USER_CREDENTIAL_EVENT *pEvent);

// Implementation of IMFPMediaPlayerCallback::OnMediaPlayerEvent
void STDMETHODCALLTYPE PlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY: 
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_PAUSE: 
        OnPause(MFP_GET_PAUSE_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_STOP: 
        OnStop(MFP_GET_STOP_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_POSITION_SET: 
        OnPositionSet(MFP_GET_POSITION_SET_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_RATE_SET: 
        OnRateSet(MFP_GET_RATE_SET_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_CREATED: 
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET: 
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_FRAME_STEP: 
        OnFrameStep(MFP_GET_FRAME_STEP_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_CLEARED: 
        OnMediaItemCleared(MFP_GET_MEDIAITEM_CLEARED_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_MF: 
        OnMFEvent(MFP_GET_MF_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_ERROR: 
        OnError(MFP_GET_ERROR_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_PLAYBACK_ENDED: 
        OnPlaybackEnded(MFP_GET_PLAYBACK_ENDED_EVENT(pEventHeader)); 
        break;

    case MFP_EVENT_TYPE_ACQUIRE_USER_CREDENTIAL: 
        OnAquireUserCredential(MFP_GET_ACQUIRE_USER_CREDENTIAL_EVENT(pEventHeader)); 
        break;
    }
}

```

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>