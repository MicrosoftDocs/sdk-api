---
UID: NF:audioenginebaseapo.IAudioSystemEffects2.GetEffectsList
title: IAudioSystemEffects2::GetEffectsList method
author: windows-driver-content
description: Gets the list of signal processing effects currently active and stores an event to be signaled if the list changes.
old-location: coreaudio\iaudiosystemeffects2_geteffectslist.htm
old-project: CoreAudio
ms.assetid: 6DA7A3F3-FE3B-4AC2-89FC-45E3D73F9DF2
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetEffectsList method [Core Audio], GetEffectsList method [Core Audio], IAudioSystemEffects2 interface, GetEffectsList,IAudioSystemEffects2.GetEffectsList, IAudioSystemEffects2, IAudioSystemEffects2 interface [Core Audio], GetEffectsList method, IAudioSystemEffects2::GetEffectsList, audioenginebaseapo/IAudioSystemEffects2::GetEffectsList, coreaudio.iaudiosystemeffects2_geteffectslist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Audioenginebaseapo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AudioClientProperties, AudioClientProperties
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audioenginebaseapo.h
api_name:
-	IAudioSystemEffects2.GetEffectsList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSystemEffects2::GetEffectsList method


## -description


Gets the list of signal processing effects currently active and stores an event to be signaled if the list changes.


## -parameters




### -param ppEffectsIds




### -param pcEffects [out]

Receives a value that specifies the number of GUIDs in <i>LPGUID</i>.


### -param Event [in]

An event handle which is signaled by the APO when the list changes.

The APO uses this event until either this function is called again or the APO is destroyed. 

<i>Event</i> may be <b>NULL</b>. If <i>Event</i> is <b>NULL</b>, the APO stops using any previous handles and does not signal an event.


#### - LPGUID [out]

Receives a pointer to a list of GUIDs.  Each GUID identifies a class of effect. 

The caller is responsible for freeing this memory by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An APO implements this method to allow Windows to discover the current effects applied by the APO. The list of effects may depend on what signal processing mode the APO initialized, see <i>AudioProcessingMode</i> in the <a href="https://msdn.microsoft.com/library/windows/hardware/dn659347">APOInitSystemEffects2</a> structure, as well as any end user configuration.

APOs should identify effects using GUIDs defined by Windows, such as <b>AUDIO_EFFECT_TYPE_ACOUSTIC_ECHO_CANCELLATION</b>. An APO should define and return a custom GUID only in rare cases where the type of effect is clearly different than one of the types defined by Windows.

If there are no effects, the function still succeeds,  but  <i>ppEffectsIds</i> returns a <b>NULL</b> pointer and <i>pcEffects</i> returns a count of 0.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn659348">IAudioSystemEffects2</a>
 

 

