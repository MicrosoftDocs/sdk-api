---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMute.SetMute
title: IAudioEndpointOffloadStreamMute::SetMute (audioengineendpoint.h)
description: The SetMute method sets the mute status of the offloaded audio stream.
helpviewer_keywords: ["IAudioEndpointOffloadStreamMute interface [Core Audio]","SetMute method","IAudioEndpointOffloadStreamMute.SetMute","IAudioEndpointOffloadStreamMute::SetMute","SetMute","SetMute method [Core Audio]","SetMute method [Core Audio]","IAudioEndpointOffloadStreamMute interface","audioengineendpoint/IAudioEndpointOffloadStreamMute::SetMute","coreaudio.iaudioendpointoffloadstreammute_setmute"]
old-location: coreaudio\iaudioendpointoffloadstreammute_setmute.htm
tech.root: CoreAudio
ms.assetid: 43AF8146-BDF6-47F5-BD8F-DA46C4624D95
ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamMute interface [Core Audio],SetMute method, IAudioEndpointOffloadStreamMute.SetMute, IAudioEndpointOffloadStreamMute::SetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],IAudioEndpointOffloadStreamMute interface, audioengineendpoint/IAudioEndpointOffloadStreamMute::SetMute, coreaudio.iaudioendpointoffloadstreammute_setmute
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAudioEndpointOffloadStreamMute::SetMute
 - audioengineendpoint/IAudioEndpointOffloadStreamMute::SetMute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamMute.SetMute
---

# IAudioEndpointOffloadStreamMute::SetMute


## -description

The <b>SetMute</b> method sets the mute status of the offloaded audio stream.

## -parameters

### -param bMuted [in]

Indicates whether or not the offloaded audio stream is to be muted. A value of <b>TRUE</b> mutes the stream, and a value of <b>FALSE</b> sets the stream to a non-muted state.

## -returns

The <b>SetMute</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointoffloadstreammute">IAudioEndpointOffloadStreamMute</a>