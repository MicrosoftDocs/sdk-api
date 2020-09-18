---
UID: NF:xapo.IXAPO.CalcOutputFrames
title: IXAPO::CalcOutputFrames (xapo.h)
description: Returns the number of output frames that will be generated from a given number of input frames.
helpviewer_keywords: ["CalcOutputFrames","CalcOutputFrames method [XAudio2 Audio Mixing APIs]","CalcOutputFrames method [XAudio2 Audio Mixing APIs]","IXAPO interface","IXAPO interface [XAudio2 Audio Mixing APIs]","CalcOutputFrames method","IXAPO.CalcOutputFrames","IXAPO::CalcOutputFrames","xapo/IXAPO::CalcOutputFrames","xaudio2.ixapo_interface_calcoutputframes"]
old-location: xaudio2\ixapo_interface_calcoutputframes.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.CalcOutputFrames(UINT32)
ms.date: 12/05/2018
ms.keywords: CalcOutputFrames, CalcOutputFrames method [XAudio2 Audio Mixing APIs], CalcOutputFrames method [XAudio2 Audio Mixing APIs],IXAPO interface, IXAPO interface [XAudio2 Audio Mixing APIs],CalcOutputFrames method, IXAPO.CalcOutputFrames, IXAPO::CalcOutputFrames, xapo/IXAPO::CalcOutputFrames, xaudio2.ixapo_interface_calcoutputframes
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAPO::CalcOutputFrames
 - xapo/IXAPO::CalcOutputFrames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPO.CalcOutputFrames
---

# IXAPO::CalcOutputFrames


## -description

Returns the number of output frames that will be generated from a given number of input frames.

## -parameters

### -param InputFrameCount

The number of input frames.

## -returns

Returns the number of output frames that will be produced.

## -remarks

XAudio2 calls this method to determine how large of an output buffer an XAPO will require for a certain number of input frames. <b>CalcOutputFrames</b> is only called by XAudio2 if the XAPO is locked.



This function should not block, because it may be called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>