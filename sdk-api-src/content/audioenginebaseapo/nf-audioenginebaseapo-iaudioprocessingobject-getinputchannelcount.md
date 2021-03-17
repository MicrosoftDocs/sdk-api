---
UID: NF:audioenginebaseapo.IAudioProcessingObject.GetInputChannelCount
title: IAudioProcessingObject::GetInputChannelCount (audioenginebaseapo.h)
description: GetInputChannelCount returns the input channel count (samples-per-frame) for this APO.
helpviewer_keywords: ["GetInputChannelCount","GetInputChannelCount method [Audio Devices]","GetInputChannelCount method [Audio Devices]","IAudioProcessingObject interface","IAudioProcessingObject interface [Audio Devices]","GetInputChannelCount method","IAudioProcessingObject.GetInputChannelCount","IAudioProcessingObject::GetInputChannelCount","audio.iaudioprocessingobject_getinputchannelcount","audioenginebaseapo/IAudioProcessingObject::GetInputChannelCount"]
old-location: audio\iaudioprocessingobject_getinputchannelcount.htm
tech.root: audio
ms.assetid: 6DB8B945-DCED-4129-A457-E90E083E6394
ms.date: 12/05/2018
ms.keywords: GetInputChannelCount, GetInputChannelCount method [Audio Devices], GetInputChannelCount method [Audio Devices],IAudioProcessingObject interface, IAudioProcessingObject interface [Audio Devices],GetInputChannelCount method, IAudioProcessingObject.GetInputChannelCount, IAudioProcessingObject::GetInputChannelCount, audio.iaudioprocessingobject_getinputchannelcount, audioenginebaseapo/IAudioProcessingObject::GetInputChannelCount
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available with Windows 7 and later Windows operating systems.
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
req.lib: Audioenginebaseapo.idl
req.dll: 
req.irql: Any level
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioProcessingObject::GetInputChannelCount
 - audioenginebaseapo/IAudioProcessingObject::GetInputChannelCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioenginebaseapo.idl
 - Audioenginebaseapo.idl.dll
api_name:
 - IAudioProcessingObject.GetInputChannelCount
---

# IAudioProcessingObject::GetInputChannelCount


## -description

GetInputChannelCount returns the input channel count (samples-per-frame) for this APO.

## -parameters

### -param pu32ChannelCount [out]

The input channel count.

## -returns

<code>GetInputChannelCount</code> returns a value of S_OK if the call was successful.

## -remarks

The input channel count that is returned refers to the input side of the APO.

## -see-also

<a href="/windows/desktop/api/audioenginebaseapo/nn-audioenginebaseapo-iaudioprocessingobject">IAudioProcessingObject</a>