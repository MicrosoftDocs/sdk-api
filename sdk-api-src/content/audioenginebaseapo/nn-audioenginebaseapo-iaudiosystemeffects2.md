---
UID: NN:audioenginebaseapo.IAudioSystemEffects2
title: IAudioSystemEffects2
author: windows-driver-content
description: Provides functionality for discovering the effects applied to an APO.
old-location: coreaudio\iaudiosystemeffects2.htm
old-project: CoreAudio
ms.assetid: 7BE71C16-CA10-4B7A-9F58-2DD75C55E8A8
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: IAudioSystemEffects2, IAudioSystemEffects2 interface [Core Audio], IAudioSystemEffects2 interface [Core Audio], described, audioenginebaseapo/IAudioSystemEffects2, coreaudio.iaudiosystemeffects2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IAudioSystemEffects2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSystemEffects2 interface


## -description


Provides functionality for  discovering the effects applied to an APO. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioSystemEffects2</b> interface inherits from IAudioSystemEffect. <b>IAudioSystemEffects2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn659349">GetEffectsList</a>
</td>
<td align="left" width="63%">
Gets the list of signal processing effects currently active and stores an event to be signaled if the list changes.

</td>
</tr>
</table> 


## -remarks



APOs support <b>IAudioSystemEffects2</b> if they support signal processing modes and effects discovery. 

When an APO supports this interface, it must accept the <a href="https://msdn.microsoft.com/library/windows/hardware/dn659347">APOInitSystemEffects2</a> structure in its implementation of <a href="https://msdn.microsoft.com/library/windows/hardware/ff536510">IAudioProcessingObject::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

