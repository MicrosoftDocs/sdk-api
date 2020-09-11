---
UID: NN:audioenginebaseapo.IAudioSystemEffects2
title: IAudioSystemEffects2 (audioenginebaseapo.h)
description: The IAudioSystemEffects2 interface was introduced with Windows 8.1 for retrieving information about the processing objects in a given mode.
helpviewer_keywords: ["IAudioSystemEffects2","IAudioSystemEffects2 interface [Audio Devices]","IAudioSystemEffects2 interface [Audio Devices]","described","audio.iaudiosystemeffects2","audioenginebaseapo/IAudioSystemEffects2"]
old-location: audio\iaudiosystemeffects2.htm
tech.root: audio
ms.assetid: 5989BAFB-6B2D-4186-9A8D-96C8974E0D18
ms.date: 12/05/2018
ms.keywords: IAudioSystemEffects2, IAudioSystemEffects2 interface [Audio Devices], IAudioSystemEffects2 interface [Audio Devices],described, audio.iaudiosystemeffects2, audioenginebaseapo/IAudioSystemEffects2
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAudioSystemEffects2
 - audioenginebaseapo/IAudioSystemEffects2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioSystemEffects2
---

# IAudioSystemEffects2 interface


## -description

The <b>IAudioSystemEffects2</b> interface was introduced with  Windows 8.1 for retrieving information about the processing objects in a given mode.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSystemEffects2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudiosystemeffects">IAudioSystemEffects</a>. <b>IAudioSystemEffects2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioSystemEffects2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffects2-geteffectslist">GetEffectsList</a>
</td>
<td align="left" width="63%">
The GetEffectsList method is used for retrieving the list of audio processing effects that are currently active, and stores an event to be signaled if the list changes.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudiosystemeffects">IAudioSystemEffects</a>

