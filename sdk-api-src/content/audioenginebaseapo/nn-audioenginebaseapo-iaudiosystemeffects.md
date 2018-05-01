---
UID: NN:audioenginebaseapo.IAudioSystemEffects
title: IAudioSystemEffects
author: windows-driver-content
description: The IAudioSystemEffects interface uses the basic methods that are inherited from IUnknown, and must implement an Initialize method.
old-location: audio\iaudiosystemeffects.htm
old-project: audio
ms.assetid: 86429c51-6831-4266-9774-1547dc04bcb0
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IAudioSystemEffects, IAudioSystemEffects interface [Audio Devices], IAudioSystemEffects interface [Audio Devices], described, audio.iaudiosystemeffects, audio_syseffects_r_bdd8290f-b7ec-4c4d-b52f-2e05e9e5c074.xml, audioenginebaseapo/IAudioSystemEffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: APO_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audioenginebaseapo.h
api_name:
-	IAudioSystemEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# IAudioSystemEffects interface


## -description


The IAudioSystemEffects  interface uses the basic methods that are inherited from <b>IUnknown</b>, and must implement an <b>Initialize</b> method. The parameters that are passed to this <b>Initialize</b> method must be passed directly to the <b>IAudioProcessingObject::Initialize</b> method.

Refer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536510">IAudioProcessingObject::Initialize</a> method for information about the structure and the parameters that are required to implement the <b>IAudioSystemEffects::Initialize</b> method.

