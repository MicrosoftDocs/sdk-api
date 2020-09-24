---
UID: NN:audioenginebaseapo.IAudioProcessingObjectRT
title: IAudioProcessingObjectRT (audioenginebaseapo.h)
description: This interface can operate in real-time mode and its methods can be called form real-time processing threads.
helpviewer_keywords: ["IAudioProcessingObjectRT","IAudioProcessingObjectRT interface [Audio Devices]","IAudioProcessingObjectRT interface [Audio Devices]","described","audio.iaudioprocessingobjectrt","audio_syseffects_r_843f0618-1708-4779-996d-7dc474a73bbf.xml","audioenginebaseapo/IAudioProcessingObjectRT"]
old-location: audio\iaudioprocessingobjectrt.htm
tech.root: audio
ms.assetid: 640ac817-16f2-47c8-87e9-1ae0136e6e55
ms.date: 12/05/2018
ms.keywords: IAudioProcessingObjectRT, IAudioProcessingObjectRT interface [Audio Devices], IAudioProcessingObjectRT interface [Audio Devices],described, audio.iaudioprocessingobjectrt, audio_syseffects_r_843f0618-1708-4779-996d-7dc474a73bbf.xml, audioenginebaseapo/IAudioProcessingObjectRT
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
 - IAudioProcessingObjectRT
 - audioenginebaseapo/IAudioProcessingObjectRT
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
 - IAudioProcessingObjectRT
---

# IAudioProcessingObjectRT interface


## -description

This interface can operate in real-time mode and its methods can be called form real-time processing threads. The implementation of the methods for this interface must not block or touch paged memory. Additionally, you must not call any blocking system routines in the implementation of the methods.

The <code>IAudioProcessingObjectRT</code> interface includes the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectrt-apoprocess">IAudioProcessingObjectRT::APOProcess</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectrt-calcinputframes">IAudioProcessingObjectRT::CalcInputFrames</a>


</dd>
<dd>

<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectrt-calcoutputframes">IAudioProcessingObjectRT::CalcOutputFrames</a>


</dd>
</dl>