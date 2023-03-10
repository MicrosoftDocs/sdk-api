---
UID: NS:xapo.XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS
title: XAPO_LOCKFORPROCESS_PARAMETERS (xapo.h)
description: Defines stream buffer parameters that remain constant while an XAPO is locked. Used with the IXAPO::LockForProcess method.
helpviewer_keywords: ["XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS","XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS structure [XAudio2 Audio Mixing APIs]","XAPO_LOCKFORPROCESS_PARAMETERS","XAPO_LOCKFORPROCESS_PARAMETERS structure [XAudio2 Audio Mixing APIs]","xapo/XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS","xaudio2.xapo_lockforprocess_buffer_parameters"]
old-location: xaudio2\xapo_lockforprocess_buffer_parameters.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapo.XAPO_LOCKFORPROCESS_PARAMETERS
ms.date: 12/05/2018
ms.keywords: XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS, XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS structure [XAudio2 Audio Mixing APIs], XAPO_LOCKFORPROCESS_PARAMETERS, XAPO_LOCKFORPROCESS_PARAMETERS structure [XAudio2 Audio Mixing APIs], xapo/XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS, xaudio2.xapo_lockforprocess_buffer_parameters
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
req.typenames: XAPO_LOCKFORPROCESS_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS
 - xapo/XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS
 - XAPO_LOCKFORPROCESS_PARAMETERS
 - xapo/XAPO_LOCKFORPROCESS_PARAMETERS
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
 - XAPO_LOCKFORPROCESS_PARAMETERS
---

# XAPO_LOCKFORPROCESS_PARAMETERS structure


## -description

Defines stream buffer parameters that remain constant while an XAPO is locked. Used with the <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudioprocessingobjectconfiguration-lockforprocess">IXAPO::LockForProcess</a> method.

## -struct-fields

### -field pFormat

A WAVFORMATEX describing the format for the stream buffer.

### -field MaxFrameCount

Maximum number of frames in the stream buffer that <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> would ever be required to handle, irrespective of dynamic parameter settings.

## -remarks

The byte size of the respective stream buffer must be at least <i>MaxFrameCount</i> × (<i>pFormat</i>-&gt;nBlockAlign) bytes.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>