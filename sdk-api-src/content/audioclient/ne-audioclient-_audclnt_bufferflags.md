---
UID: NE:audioclient._AUDCLNT_BUFFERFLAGS
title: _AUDCLNT_BUFFERFLAGS (audioclient.h)
description: The _AUDCLNT_BUFFERFLAGS enumeration defines flags that indicate the status of an audio endpoint buffer.
helpviewer_keywords: ["AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY","AUDCLNT_BUFFERFLAGS_SILENT","AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR","_AUDCLNT_BUFFERFLAGS","_AUDCLNT_BUFFERFLAGS","_AUDCLNT_BUFFERFLAGS enumeration [Core Audio]","audioclient/AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY","audioclient/AUDCLNT_BUFFERFLAGS_SILENT","audioclient/AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR","audioclient/_AUDCLNT_BUFFERFLAGS","coreaudio._audclnt_bufferflags"]
old-location: coreaudio\_audclnt_bufferflags.htm
tech.root: CoreAudio
ms.assetid: ac4ec901-b1e2-4c4e-b9fc-1808d5338d15
ms.date: 12/05/2018
ms.keywords: AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY, AUDCLNT_BUFFERFLAGS_SILENT, AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR, _AUDCLNT_BUFFERFLAGS, _AUDCLNT_BUFFERFLAGS , _AUDCLNT_BUFFERFLAGS enumeration [Core Audio], audioclient/AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY, audioclient/AUDCLNT_BUFFERFLAGS_SILENT, audioclient/AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR, audioclient/_AUDCLNT_BUFFERFLAGS, coreaudio._audclnt_bufferflags
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - _AUDCLNT_BUFFERFLAGS
 - audioclient/_AUDCLNT_BUFFERFLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioclient.h
api_name:
 - _AUDCLNT_BUFFERFLAGS
---

# _AUDCLNT_BUFFERFLAGS enumeration


## -description

The <b>_AUDCLNT_BUFFERFLAGS</b> enumeration defines flags that indicate the status of an audio endpoint buffer.

## -enum-fields

### -field AUDCLNT_BUFFERFLAGS_DATA_DISCONTINUITY

The data in the packet is not correlated with the previous packet's device position; this is possibly due to a stream state transition or timing glitch.

### -field AUDCLNT_BUFFERFLAGS_SILENT

Treat all of the data in the packet as silence and ignore the actual data values. For more information about the use of this flag, see <a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a> and <a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>.

### -field AUDCLNT_BUFFERFLAGS_TIMESTAMP_ERROR

The time at which the device's stream position was recorded is uncertain. Thus, the client might be unable to accurately set the time stamp for the current data packet.

## -remarks

The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> and <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a> methods use the constants defined in the <b>_AUDCLNT_BUFFERFLAGS</b> enumeration.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a>