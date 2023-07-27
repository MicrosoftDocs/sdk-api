---
UID: NF:vmr9.IVMRVideoStreamControl9.SetStreamActiveState
title: IVMRVideoStreamControl9::SetStreamActiveState (vmr9.h)
description: The SetStreamActiveState method activates or inactivates an input stream.
helpviewer_keywords: ["IVMRVideoStreamControl9 interface [DirectShow]","SetStreamActiveState method","IVMRVideoStreamControl9.SetStreamActiveState","IVMRVideoStreamControl9::SetStreamActiveState","IVMRVideoStreamControl9SetStreamActiveState","SetStreamActiveState","SetStreamActiveState method [DirectShow]","SetStreamActiveState method [DirectShow]","IVMRVideoStreamControl9 interface","dshow.ivmrvideostreamcontrol9_setstreamactivestate","vmr9/IVMRVideoStreamControl9::SetStreamActiveState"]
old-location: dshow\ivmrvideostreamcontrol9_setstreamactivestate.htm
tech.root: dshow
ms.assetid: 2c17a006-f086-49cd-a237-3713fb9bd3f9
ms.date: 4/26/2023
ms.keywords: IVMRVideoStreamControl9 interface [DirectShow],SetStreamActiveState method, IVMRVideoStreamControl9.SetStreamActiveState, IVMRVideoStreamControl9::SetStreamActiveState, IVMRVideoStreamControl9SetStreamActiveState, SetStreamActiveState, SetStreamActiveState method [DirectShow], SetStreamActiveState method [DirectShow],IVMRVideoStreamControl9 interface, dshow.ivmrvideostreamcontrol9_setstreamactivestate, vmr9/IVMRVideoStreamControl9::SetStreamActiveState
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRVideoStreamControl9::SetStreamActiveState
 - vmr9/IVMRVideoStreamControl9::SetStreamActiveState
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
 - IVMRVideoStreamControl9.SetStreamActiveState
---

# IVMRVideoStreamControl9::SetStreamActiveState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetStreamActiveState</code> method activates or inactivates an input stream.

## -parameters

### -param fActive [in]

Specifies the state of the stream. <b>TRUE</b> means active; <b>FALSE</b> means inactive.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrvideostreamcontrol9">IVMRVideoStreamControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>