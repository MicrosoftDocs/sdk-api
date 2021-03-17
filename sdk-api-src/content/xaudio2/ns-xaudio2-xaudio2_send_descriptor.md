---
UID: NS:xaudio2.XAUDIO2_SEND_DESCRIPTOR
title: XAUDIO2_SEND_DESCRIPTOR (xaudio2.h)
description: Defines a destination voice that is the target of a send from another voice and specifies whether a filter should be used.
helpviewer_keywords: ["XAUDIO2_SEND_DESCRIPTOR","XAUDIO2_SEND_DESCRIPTOR structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_send_descriptor","xaudio2/XAUDIO2_SEND_DESCRIPTOR"]
old-location: xaudio2\xaudio2_send_descriptor.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_SEND_DESCRIPTOR
ms.date: 12/05/2018
ms.keywords: XAUDIO2_SEND_DESCRIPTOR, XAUDIO2_SEND_DESCRIPTOR structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_send_descriptor, xaudio2/XAUDIO2_SEND_DESCRIPTOR
req.header: xaudio2.h
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
req.typenames: XAUDIO2_SEND_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_SEND_DESCRIPTOR
 - xaudio2/XAUDIO2_SEND_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_SEND_DESCRIPTOR
---

# XAUDIO2_SEND_DESCRIPTOR structure


## -description

Defines a destination voice that is the target of a send from another voice and specifies whether a filter should be used.

## -struct-fields

### -field Flags

Indicates whether a filter should be used on data sent to the voice pointed to by <b>pOutputVoice</b>. Flags can be 0 or XAUDIO2_SEND_USEFILTER.

### -field pOutputVoice

A pointer to an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice">IXAudio2Voice</a> that will be the target of the send. The <b>pOutputVoice</b> member cannot be NULL.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--change-voice-volume">How to: Change Voice Volume</a>



<a href="/windows/desktop/xaudio2/how-to--use-submix-voices">How to: Use Submix Voices</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">IXAudio2::CreateSourceVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice">IXAudio2::CreateSubmixVoice</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices">IXAudio2Voice::SetOutputVoices</a>



<a href="/windows/desktop/xaudio2/structures">XAudio Structures</a>



<a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a>