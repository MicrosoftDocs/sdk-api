---
UID: NF:audiopolicy.IAudioSessionEnumerator.GetCount
title: IAudioSessionEnumerator::GetCount (audiopolicy.h)
description: The GetCount method gets the total number of audio sessions that are open on the audio device.
helpviewer_keywords: ["GetCount","GetCount method [Core Audio]","GetCount method [Core Audio]","IAudioSessionEnumerator interface","IAudioSessionEnumerator interface [Core Audio]","GetCount method","IAudioSessionEnumerator.GetCount","IAudioSessionEnumerator::GetCount","audiopolicy/IAudioSessionEnumerator::GetCount","coreaudio.iaudiosessionenumerator_getcount"]
old-location: coreaudio\iaudiosessionenumerator_getcount.htm
tech.root: CoreAudio
ms.assetid: a1fbfbf5-a79b-40bc-97c7-a76a181bbfec
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Core Audio], GetCount method [Core Audio],IAudioSessionEnumerator interface, IAudioSessionEnumerator interface [Core Audio],GetCount method, IAudioSessionEnumerator.GetCount, IAudioSessionEnumerator::GetCount, audiopolicy/IAudioSessionEnumerator::GetCount, coreaudio.iaudiosessionenumerator_getcount
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
 - IAudioSessionEnumerator::GetCount
 - audiopolicy/IAudioSessionEnumerator::GetCount
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
 - IAudioSessionEnumerator.GetCount
---

# IAudioSessionEnumerator::GetCount


## -description

The <b>GetCount</b> method gets the total number of audio sessions that are open on the audio device.

## -parameters

### -param SessionCount [out]

Receives the total number of audio sessions.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator">IAudioSessionEnumerator</a>