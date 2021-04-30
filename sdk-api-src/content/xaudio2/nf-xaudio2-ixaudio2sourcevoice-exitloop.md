---
UID: NF:xaudio2.IXAudio2SourceVoice.ExitLoop
title: IXAudio2SourceVoice::ExitLoop (xaudio2.h)
description: Stops looping the voice when it reaches the end of the current loop region.
helpviewer_keywords: ["ExitLoop","ExitLoop method [XAudio2 Audio Mixing APIs]","ExitLoop method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","ExitLoop method","IXAudio2SourceVoice.ExitLoop","IXAudio2SourceVoice::ExitLoop","xaudio2.ixaudio2sourcevoice_interface_exitloop","xaudio2/IXAudio2SourceVoice::ExitLoop"]
old-location: xaudio2\ixaudio2sourcevoice_interface_exitloop.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.ExitLoop(UINT32)
ms.date: 12/05/2018
ms.keywords: ExitLoop, ExitLoop method [XAudio2 Audio Mixing APIs], ExitLoop method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],ExitLoop method, IXAudio2SourceVoice.ExitLoop, IXAudio2SourceVoice::ExitLoop, xaudio2.ixaudio2sourcevoice_interface_exitloop, xaudio2/IXAudio2SourceVoice::ExitLoop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2SourceVoice::ExitLoop
 - xaudio2/IXAudio2SourceVoice::ExitLoop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.ExitLoop
---

# IXAudio2SourceVoice::ExitLoop


## -description

Stops looping the voice when it reaches the end of the current loop region.

## -parameters

### -param X2DEFAULT [in]

Identifies this call as part of a deferred batch. See the <a href="/windows/desktop/xaudio2/xaudio2-operation-sets">XAudio2 Operation Sets</a> overview for more information.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

If the cursor for the voice is not in a loop region, <b>ExitLoop</b> does nothing.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>