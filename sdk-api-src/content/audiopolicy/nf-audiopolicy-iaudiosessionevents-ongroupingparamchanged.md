---
UID: NF:audiopolicy.IAudioSessionEvents.OnGroupingParamChanged
title: IAudioSessionEvents::OnGroupingParamChanged (audiopolicy.h)
description: The OnGroupingParamChanged method notifies the client that the grouping parameter for the session has changed.
helpviewer_keywords: ["IAudioSessionEvents interface [Core Audio]","OnGroupingParamChanged method","IAudioSessionEvents.OnGroupingParamChanged","IAudioSessionEvents::OnGroupingParamChanged","IAudioSessionEventsOnGroupingParamChanged","OnGroupingParamChanged","OnGroupingParamChanged method [Core Audio]","OnGroupingParamChanged method [Core Audio]","IAudioSessionEvents interface","audiopolicy/IAudioSessionEvents::OnGroupingParamChanged","coreaudio.iaudiosessionevents_ongroupingparamchanged"]
old-location: coreaudio\iaudiosessionevents_ongroupingparamchanged.htm
tech.root: CoreAudio
ms.assetid: f52c9d8a-245b-489a-81c1-cb4715faa8be
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnGroupingParamChanged method, IAudioSessionEvents.OnGroupingParamChanged, IAudioSessionEvents::OnGroupingParamChanged, IAudioSessionEventsOnGroupingParamChanged, OnGroupingParamChanged, OnGroupingParamChanged method [Core Audio], OnGroupingParamChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnGroupingParamChanged, coreaudio.iaudiosessionevents_ongroupingparamchanged
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioSessionEvents::OnGroupingParamChanged
 - audiopolicy/IAudioSessionEvents::OnGroupingParamChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionEvents.OnGroupingParamChanged
---

# IAudioSessionEvents::OnGroupingParamChanged


## -description

The <b>OnGroupingParamChanged</b> method notifies the client that the grouping parameter for the session has changed.

## -parameters

### -param NewGroupingParam [in]

The new grouping parameter for the session. This parameter points to a grouping-parameter GUID.

### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam">IAudioSessionControl::SetGroupingParam</a> in the call that changed the grouping parameter for the session. For more information, see Remarks.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The session manager calls this method each time a call to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam">IAudioSessionControl::SetGroupingParam</a> method changes the grouping parameter for the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a grouping-parameter change that it initiated and one that some other client initiated. When calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam">IAudioSessionControl::SetGroupingParam</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnGroupingParamChanged</b> method can recognize.

For a code example that implements the methods in the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam">IAudioSessionControl::SetGroupingParam</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>