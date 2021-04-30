---
UID: NS:xapo.XAPO_PROCESS_BUFFER_PARAMETERS
title: XAPO_PROCESS_BUFFER_PARAMETERS (xapo.h)
description: Defines stream buffer parameters that may change from one call to the next. Used with the Process method.
helpviewer_keywords: ["XAPO_PROCESS_BUFFER_PARAMETERS","XAPO_PROCESS_BUFFER_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapo/XAPO_PROCESS_BUFFER_PARAMETERS","xaudio2.xapo_process_buffer_parameters"]
old-location: xaudio2\xapo_process_buffer_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapo.XAPO_PROCESS_BUFFER_PARAMETERS
ms.date: 12/05/2018
ms.keywords: XAPO_PROCESS_BUFFER_PARAMETERS, XAPO_PROCESS_BUFFER_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapo/XAPO_PROCESS_BUFFER_PARAMETERS, xaudio2.xapo_process_buffer_parameters
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
req.typenames: XAPO_PROCESS_BUFFER_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAPO_PROCESS_BUFFER_PARAMETERS
 - xapo/XAPO_PROCESS_BUFFER_PARAMETERS
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
 - XAPO_PROCESS_BUFFER_PARAMETERS
---

# XAPO_PROCESS_BUFFER_PARAMETERS structure


## -description

Defines stream buffer parameters that may change from one call to the next. Used with the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">Process</a> method.

## -struct-fields

### -field pBuffer

Pointer to a stream buffer that contains audio data. The buffer must be 16-byte aligned, non-NULL, and must be at least <a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a>.MaxFrameCount frames in size.

### -field BufferFlags

An <a href="/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags">XAPO_BUFFER_FLAGS</a> enumeration describing the contents of the stream buffer.

### -field ValidFrameCount

Number of frames to process; this value must be within the range 0 to <a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a>.MaxFrameCount.

## -remarks

Although the format and maximum size values of a particular stream buffer are constant, as defined by the <a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a> structure, the actual memory address of the stream buffer is permitted to change. For constant-bit-rate (CBR) XAPOs, ValidFrameCount is constant and is always equal to the corresponding <b>XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</b>.MaxFrameCount for this buffer.

<div class="alert"><b>Note</b>  Only constant-bit-rate XAPOs are currently supported.</div>
<div> </div>


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>