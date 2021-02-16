---
UID: NF:audiopolicy.IAudioSessionEnumerator.GetSession
title: IAudioSessionEnumerator::GetSession (audiopolicy.h)
description: The GetSession method gets the audio session specified by an audio session number.
helpviewer_keywords: ["GetSession","GetSession method [Core Audio]","GetSession method [Core Audio]","IAudioSessionEnumerator interface","IAudioSessionEnumerator interface [Core Audio]","GetSession method","IAudioSessionEnumerator.GetSession","IAudioSessionEnumerator::GetSession","audiopolicy/IAudioSessionEnumerator::GetSession","coreaudio.iaudiosessionenumerator_getsession"]
old-location: coreaudio\iaudiosessionenumerator_getsession.htm
tech.root: CoreAudio
ms.assetid: 45b7af16-aca0-49f8-b977-f7e4f1885687
ms.date: 12/05/2018
ms.keywords: GetSession, GetSession method [Core Audio], GetSession method [Core Audio],IAudioSessionEnumerator interface, IAudioSessionEnumerator interface [Core Audio],GetSession method, IAudioSessionEnumerator.GetSession, IAudioSessionEnumerator::GetSession, audiopolicy/IAudioSessionEnumerator::GetSession, coreaudio.iaudiosessionenumerator_getsession
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
 - IAudioSessionEnumerator::GetSession
 - audiopolicy/IAudioSessionEnumerator::GetSession
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
 - IAudioSessionEnumerator.GetSession
---

# IAudioSessionEnumerator::GetSession


## -description

The <b>GetSession</b> method gets the audio session specified by an audio session number.

## -parameters

### -param SessionCount [in]

The session number. If there are <i>n</i> sessions, the sessions are numbered from 0 to <i>n</i> – 1. To get the number of sessions, call the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionenumerator-getcount">IAudioSessionEnumerator::GetCount</a> method.

### -param Session [out]

Receives a pointer to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl</a> interface of the session object in the collection that is maintained by the session enumerator. The caller must release the interface pointer.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator</a>