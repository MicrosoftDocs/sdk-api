---
UID: NF:xapo.IXAPO.CalcInputFrames
title: IXAPO::CalcInputFrames (xapo.h)
description: Returns the number of input frames required to generate the given number of output frames.
helpviewer_keywords: ["CalcInputFrames","CalcInputFrames method [XAudio2 Audio Mixing APIs]","CalcInputFrames method [XAudio2 Audio Mixing APIs]","IXAPO interface","IXAPO interface [XAudio2 Audio Mixing APIs]","CalcInputFrames method","IXAPO.CalcInputFrames","IXAPO::CalcInputFrames","xapo/IXAPO::CalcInputFrames","xaudio2.ixapo_interface_calcinputframes"]
old-location: xaudio2\ixapo_interface_calcinputframes.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapo.IXAPO.CalcInputFrames(UINT32)
ms.date: 12/05/2018
ms.keywords: CalcInputFrames, CalcInputFrames method [XAudio2 Audio Mixing APIs], CalcInputFrames method [XAudio2 Audio Mixing APIs],IXAPO interface, IXAPO interface [XAudio2 Audio Mixing APIs],CalcInputFrames method, IXAPO.CalcInputFrames, IXAPO::CalcInputFrames, xapo/IXAPO::CalcInputFrames, xaudio2.ixapo_interface_calcinputframes
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
 - IXAPO::CalcInputFrames
 - xapo/IXAPO::CalcInputFrames
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
 - IXAPO.CalcInputFrames
---

# IXAPO::CalcInputFrames


## -description

Returns the number of input frames required to generate the given number of output frames.

## -parameters

### -param OutputFrameCount

The number of output frames desired.

## -returns

Returns the number of input frames required.

## -remarks

XAudio2 calls this method to determine what size input buffer an XAPO requires to generate the given number of output frames. This method only needs to be called once while an XAPO is locked. <b>CalcInputFrames</b> is only called by XAudio2 if the XAPO is locked.



This function should not block, because it may be called from the realtime audio processing thread.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>