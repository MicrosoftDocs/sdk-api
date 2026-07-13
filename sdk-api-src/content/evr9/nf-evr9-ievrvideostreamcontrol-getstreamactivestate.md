---
UID: NF:evr9.IEVRVideoStreamControl.GetStreamActiveState
title: IEVRVideoStreamControl::GetStreamActiveState (evr9.h)
description: IEVRVideoStreamControl::GetStreamActiveState method
helpviewer_keywords: ["GetStreamActiveState","GetStreamActiveState method [Media Foundation]","GetStreamActiveState method [Media Foundation]","IEVRVideoStreamControl interface","IEVRVideoStreamControl interface [Media Foundation]","GetStreamActiveState method","IEVRVideoStreamControl.GetStreamActiveState","IEVRVideoStreamControl::GetStreamActiveState","d4ca1da7-7768-45b4-a0be-f3ef86fed7b9","evr9/IEVRVideoStreamControl::GetStreamActiveState","mf.ievrvideostreamcontrol_getstreamactivestate"]
old-location: mf\ievrvideostreamcontrol_getstreamactivestate.htm
tech.root: mfarchive
ms.assetid: d4ca1da7-7768-45b4-a0be-f3ef86fed7b9
ms.date: 12/05/2018
ms.keywords: GetStreamActiveState, GetStreamActiveState method [Media Foundation], GetStreamActiveState method [Media Foundation],IEVRVideoStreamControl interface, IEVRVideoStreamControl interface [Media Foundation],GetStreamActiveState method, IEVRVideoStreamControl.GetStreamActiveState, IEVRVideoStreamControl::GetStreamActiveState, d4ca1da7-7768-45b4-a0be-f3ef86fed7b9, evr9/IEVRVideoStreamControl::GetStreamActiveState, mf.ievrvideostreamcontrol_getstreamactivestate
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRVideoStreamControl::GetStreamActiveState
 - evr9/IEVRVideoStreamControl::GetStreamActiveState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IEVRVideoStreamControl.GetStreamActiveState
archived: true
---

# IEVRVideoStreamControl::GetStreamActiveState


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

<div class="alert"><b>Note</b>  This method is not supported.</div><div> </div>

## -parameters

### -param lpfActive [out]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol">IEVRVideoStreamControl</a>