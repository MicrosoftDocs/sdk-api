---
UID: NF:audioenginebaseapo.IAudioSystemEffects2.GetEffectsList
title: IAudioSystemEffects2::GetEffectsList (audioenginebaseapo.h)
description: The GetEffectsList method is used for retrieving the list of audio processing effects that are currently active, and stores an event to be signaled if the list changes.
helpviewer_keywords: ["GetEffectsList","GetEffectsList method [Audio Devices]","GetEffectsList method [Audio Devices]","IAudioSystemEffects2 interface","IAudioSystemEffects2 interface [Audio Devices]","GetEffectsList method","IAudioSystemEffects2.GetEffectsList","IAudioSystemEffects2::GetEffectsList","audio.iaudiosystemeffects2_geteffectslist","audioenginebaseapo/IAudioSystemEffects2::GetEffectsList"]
old-location: audio\iaudiosystemeffects2_geteffectslist.htm
tech.root: audio
ms.assetid: FC337D99-E992-43DB-9565-3B46827A7960
ms.date: 12/05/2018
ms.keywords: GetEffectsList, GetEffectsList method [Audio Devices], GetEffectsList method [Audio Devices],IAudioSystemEffects2 interface, IAudioSystemEffects2 interface [Audio Devices],GetEffectsList method, IAudioSystemEffects2.GetEffectsList, IAudioSystemEffects2::GetEffectsList, audio.iaudiosystemeffects2_geteffectslist, audioenginebaseapo/IAudioSystemEffects2::GetEffectsList
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Desktop
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
 - IAudioSystemEffects2::GetEffectsList
 - audioenginebaseapo/IAudioSystemEffects2::GetEffectsList
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
 - IAudioSystemEffects2.GetEffectsList
---

# IAudioSystemEffects2::GetEffectsList


## -description

The GetEffectsList method is used for retrieving the list of audio processing effects that are currently active, and stores an event to be signaled if the list changes.

## -parameters

### -param ppEffectsIds [out]

Pointer to the list of GUIDs that represent audio processing effects. The caller is responsible for freeing this memory by calling CoTaskMemFree.

### -param pcEffects [out]

A count of the audio processing effects in the list.

### -param Event [in]

The HANDLE of the event that will be signaled if the list changes.

## -returns

The <b>GetEffectsList</b> method returns S_OK, If the method call is successful. If there are no effects in the list, the function still succeeds, <i>ppEffectsIds</i> returns a NULL pointer, and <i>pcEffects</i> returns a count of 0.

## -remarks

The APO signals the specified  event when the list of audio processing effects changes from the list that was returned by <b>GetEffectsList</b>. The APO uses this event until either <b>GetEffectsList</b> is called again, or the APO is destroyed. The passed handle can be NULL, in which case the APO stops using any previous handle and does not signal an event.

An APO implements this method to allow Windows to discover the current effects applied by the APO. The list of effects may depend on the processing mode that the APO initialized, and on any end user configuration. The processing mode is indicated by the <i>AudioProcessingMode</i> member of <a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2">APOInitSystemEffects2</a>.

APOs should identify effects using GUIDs defined by Windows, such as AUDIO_EFFECT_TYPE_ACOUSTIC_ECHO_CANCELLATION. An APO should only define and return a custom GUID in rare cases where the type of effect is clearly different from the ones defined by Windows.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects2">APOInitSystemEffects2</a>



<a href="/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudiosystemeffects2">IAudioSystemEffects2</a>