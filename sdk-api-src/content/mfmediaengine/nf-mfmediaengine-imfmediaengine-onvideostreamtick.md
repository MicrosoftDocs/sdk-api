---
UID: NF:mfmediaengine.IMFMediaEngine.OnVideoStreamTick
title: IMFMediaEngine::OnVideoStreamTick (mfmediaengine.h)
description: Queries the Media Engine to find out whether a new video frame is ready.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","OnVideoStreamTick method","IMFMediaEngine.OnVideoStreamTick","IMFMediaEngine::OnVideoStreamTick","OnVideoStreamTick","OnVideoStreamTick method [Media Foundation]","OnVideoStreamTick method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_onvideostreamtick","mfmediaengine/IMFMediaEngine::OnVideoStreamTick"]
old-location: mf\imfmediaengine_onvideostreamtick.htm
tech.root: mf
ms.assetid: EC06D3D6-F103-4932-96C1-B55A59CD5E34
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],OnVideoStreamTick method, IMFMediaEngine.OnVideoStreamTick, IMFMediaEngine::OnVideoStreamTick, OnVideoStreamTick, OnVideoStreamTick method [Media Foundation], OnVideoStreamTick method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_onvideostreamtick, mfmediaengine/IMFMediaEngine::OnVideoStreamTick
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngine::OnVideoStreamTick
 - mfmediaengine/IMFMediaEngine::OnVideoStreamTick
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.OnVideoStreamTick
---

# IMFMediaEngine::OnVideoStreamTick


## -description

Queries the Media Engine to find out whether a new video frame is ready.

## -parameters

### -param pPts [out]

If a new frame is ready, receives the presentation time of the frame.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but the Media Engine does not have a new frame.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
A new video frame is ready for display.

</td>
</tr>
</table>

## -remarks

In frame-server mode, the application should call this method whenever a vertical blank occurs in the display device. If the method returns <b>S_OK</b>, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-transfervideoframe">IMFMediaEngine::TransferVideoFrame</a> to blit the frame to the render target. If the method returns <b>S_FALSE</b>, wait for the next vertical blank and call the method again.

Do not call this method in rendering mode or audio-only mode.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>