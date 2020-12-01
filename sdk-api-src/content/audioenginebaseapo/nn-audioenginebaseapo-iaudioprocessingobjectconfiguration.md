---
UID: NN:audioenginebaseapo.IAudioProcessingObjectConfiguration
title: IAudioProcessingObjectConfiguration (audioenginebaseapo.h)
description: The IAudioProcessingObjectConfiguration interface is used to configure the APO. This interface uses its methods to lock and unlock the APO for processing.
helpviewer_keywords: ["IAudioProcessingObjectConfiguration","IAudioProcessingObjectConfiguration interface [Audio Devices]","IAudioProcessingObjectConfiguration interface [Audio Devices]","described","audio.iaudioprocessingobjectconfiguration","audio_syseffects_r_b3847e21-94ea-45b3-9ae4-ccdb83f262aa.xml","audioenginebaseapo/IAudioProcessingObjectConfiguration"]
old-location: audio\iaudioprocessingobjectconfiguration.htm
tech.root: audio
ms.assetid: 6311a5d1-b9d3-4c62-99aa-8feda32b4a2f
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObjectConfiguration, IAudioProcessingObjectConfiguration interface [Audio Devices], IAudioProcessingObjectConfiguration interface [Audio Devices],described, audio.iaudioprocessingobjectconfiguration, audio_syseffects_r_b3847e21-94ea-45b3-9ae4-ccdb83f262aa.xml, audioenginebaseapo/IAudioProcessingObjectConfiguration
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
 - IAudioProcessingObjectConfiguration
 - audioenginebaseapo/IAudioProcessingObjectConfiguration
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
 - IAudioProcessingObjectConfiguration
---

# IAudioProcessingObjectConfiguration interface


## -description

The <code>IAudioProcessingObjectConfiguration</code> interface is used to configure the APO. This interface uses its methods to lock and unlock the APO for processing.

The <code>IAudioProcessingObjectConfiguration</code> interface supports the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectconfiguration-lockforprocess">IAudioProcessingObjectConfiguration::LockForProcess</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectconfiguration-unlockforprocess">IAudioProcessingObjectConfiguration::UnlockForProcess</a>


</dd>
</dl>