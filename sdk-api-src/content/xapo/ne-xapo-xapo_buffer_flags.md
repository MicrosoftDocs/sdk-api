---
UID: NE:xapo.XAPO_BUFFER_FLAGS
title: XAPO_BUFFER_FLAGS (xapo.h)
description: Describes the contents of a stream buffer.
helpviewer_keywords: ["XAPO_BUFFER_FLAGS","XAPO_BUFFER_FLAGS enumeration [XAudio2 Audio Mixing APIs]","XAPO_BUFFER_SILENT","XAPO_BUFFER_VALID","xapo/XAPO_BUFFER_FLAGS","xapo/XAPO_BUFFER_SILENT","xapo/XAPO_BUFFER_VALID","xaudio2.xapo_buffer_flags"]
old-location: xaudio2\xapo_buffer_flags.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapo.XAPO_BUFFER_FLAGS
ms.date: 12/05/2018
ms.keywords: XAPO_BUFFER_FLAGS, XAPO_BUFFER_FLAGS enumeration [XAudio2 Audio Mixing APIs], XAPO_BUFFER_SILENT, XAPO_BUFFER_VALID, xapo/XAPO_BUFFER_FLAGS, xapo/XAPO_BUFFER_SILENT, xapo/XAPO_BUFFER_VALID, xaudio2.xapo_buffer_flags
req.header: xapo.h
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
req.typenames: XAPO_BUFFER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAPO_BUFFER_FLAGS
 - xapo/XAPO_BUFFER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapo.h
api_name:
 - XAPO_BUFFER_FLAGS
---

# XAPO_BUFFER_FLAGS enumeration


## -description

Describes the contents of a stream buffer.

## -enum-fields

### -field XAPO_BUFFER_SILENT

Stream buffer contains only silent samples.

### -field XAPO_BUFFER_VALID

Stream buffer contains audio data to be processed.

## -remarks

This metadata can be used to implement optimizations that require knowledge of a stream buffer's contents. For example, XAPOs that always produce silent output from silent input can check the flag on the input stream buffer to determine if any signal processing is necessary. If silent, the XAPO can simply set the flag on the output stream buffer to silent and return, thus averting the work of processing silent data.



Likewise, XAPOs that receive valid input data, but generate silence (for any reason), may set the output stream buffer's flag accordingly, rather than writing silent samples to the buffer.



These flags represent what should be assumed is in the respective buffer. The flags may not reflect what is actually stored in memory. For example, the XAPO_BUFFER_SILENT indicates that silent data should be assumed, however the respective memory may be uninitialized



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/enumerations">Enumerations</a>