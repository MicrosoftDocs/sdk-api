---
UID: NF:mfmediaengine.IMFTimedTextNotify.Cue
title: IMFTimedTextNotify::Cue (mfmediaengine.h)
description: Called when a cue event occurs in a text track.
helpviewer_keywords: ["Cue","Cue method [Media Foundation]","Cue method [Media Foundation]","IMFTimedTextNotify interface","IMFTimedTextNotify interface [Media Foundation]","Cue method","IMFTimedTextNotify.Cue","IMFTimedTextNotify::Cue","mf.imftimedtextnotify_cue","mfmediaengine/IMFTimedTextNotify::Cue"]
old-location: mf\imftimedtextnotify_cue.htm
tech.root: mf
ms.assetid: EE577250-2D75-4130-BA50-95D3E455A574
ms.date: 12/05/2018
ms.keywords: Cue, Cue method [Media Foundation], Cue method [Media Foundation],IMFTimedTextNotify interface, IMFTimedTextNotify interface [Media Foundation],Cue method, IMFTimedTextNotify.Cue, IMFTimedTextNotify::Cue, mf.imftimedtextnotify_cue, mfmediaengine/IMFTimedTextNotify::Cue
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFTimedTextNotify::Cue
 - mfmediaengine/IMFTimedTextNotify::Cue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextNotify.Cue
---

# IMFTimedTextNotify::Cue


## -description

Called when a cue event occurs in a text track.

## -parameters

### -param cueEvent [in]

Type: <b><a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_timed_text_cue_event">MF_TIMED_TEXT_CUE_EVENT</a></b>

A value specifying the type of event that has occurred.

### -param currentTime [in]

Type: <b>double</b>

The current time when the cue event occurred.

### -param cue [in]

Type: <b><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>*</b>

The <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a> object representing the cue.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify">IMFTimedTextNotify</a>