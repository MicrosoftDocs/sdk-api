---
UID: NN:audioenginebaseapo.IAudioSystemEffects
title: IAudioSystemEffects (audioenginebaseapo.h)
description: The IAudioSystemEffects interface uses the basic methods that are inherited from IUnknown, and must implement an Initialize method.
helpviewer_keywords: ["IAudioSystemEffects","IAudioSystemEffects interface [Audio Devices]","IAudioSystemEffects interface [Audio Devices]","described","audio.iaudiosystemeffects","audio_syseffects_r_bdd8290f-b7ec-4c4d-b52f-2e05e9e5c074.xml","audioenginebaseapo/IAudioSystemEffects"]
old-location: audio\iaudiosystemeffects.htm
tech.root: audio
ms.assetid: 86429c51-6831-4266-9774-1547dc04bcb0
ms.date: 12/05/2018
ms.keywords: IAudioSystemEffects, IAudioSystemEffects interface [Audio Devices], IAudioSystemEffects interface [Audio Devices],described, audio.iaudiosystemeffects, audio_syseffects_r_bdd8290f-b7ec-4c4d-b52f-2e05e9e5c074.xml, audioenginebaseapo/IAudioSystemEffects
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
 - IAudioSystemEffects
 - audioenginebaseapo/IAudioSystemEffects
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
 - IAudioSystemEffects
---

# IAudioSystemEffects interface


## -description

The IAudioSystemEffects  interface uses the basic methods that are inherited from <b>IUnknown</b>, and must implement an <b>Initialize</b> method. The parameters that are passed to this <b>Initialize</b> method must be passed directly to the <b>IAudioProcessingObject::Initialize</b> method.

Refer to the <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobject-initialize">IAudioProcessingObject::Initialize</a> method for information about the structure and the parameters that are required to implement the <b>IAudioSystemEffects::Initialize</b> method.