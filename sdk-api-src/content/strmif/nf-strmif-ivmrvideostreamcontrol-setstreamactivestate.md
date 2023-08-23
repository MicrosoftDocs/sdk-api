---
UID: NF:strmif.IVMRVideoStreamControl.SetStreamActiveState
title: IVMRVideoStreamControl::SetStreamActiveState (strmif.h)
description: The SetStreamActiveState method activates or inactivates an input stream.
helpviewer_keywords: ["IVMRVideoStreamControl interface [DirectShow]","SetStreamActiveState method","IVMRVideoStreamControl.SetStreamActiveState","IVMRVideoStreamControl::SetStreamActiveState","IVMRVideoStreamControlSetStreamActiveState","SetStreamActiveState","SetStreamActiveState method [DirectShow]","SetStreamActiveState method [DirectShow]","IVMRVideoStreamControl interface","dshow.ivmrvideostreamcontrol_setstreamactivestate","strmif/IVMRVideoStreamControl::SetStreamActiveState"]
old-location: dshow\ivmrvideostreamcontrol_setstreamactivestate.htm
tech.root: dshow
ms.assetid: 060a95a4-b984-40c6-afe8-136df96c353e
ms.date: 4/26/2023
ms.keywords: IVMRVideoStreamControl interface [DirectShow],SetStreamActiveState method, IVMRVideoStreamControl.SetStreamActiveState, IVMRVideoStreamControl::SetStreamActiveState, IVMRVideoStreamControlSetStreamActiveState, SetStreamActiveState, SetStreamActiveState method [DirectShow], SetStreamActiveState method [DirectShow],IVMRVideoStreamControl interface, dshow.ivmrvideostreamcontrol_setstreamactivestate, strmif/IVMRVideoStreamControl::SetStreamActiveState
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRVideoStreamControl::SetStreamActiveState
 - strmif/IVMRVideoStreamControl::SetStreamActiveState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRVideoStreamControl.SetStreamActiveState
---

# IVMRVideoStreamControl::SetStreamActiveState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetStreamActiveState</code> method activates or inactivates an input stream.

## -parameters

### -param fActive [in]

Specifies the state of the stream. <b>TRUE</b> means active; <b>FALSE</b> means inactive.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrvideostreamcontrol">IVMRVideoStreamControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate">IVMRVideoStreamControl::GetStreamActiveState</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>