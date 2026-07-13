---
UID: NF:strmif.IVMRImageCompositor.TermCompositionTarget
title: IVMRImageCompositor::TermCompositionTarget (strmif.h)
description: The TermCompositionTarget method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.
helpviewer_keywords: ["IVMRImageCompositor interface [DirectShow]","TermCompositionTarget method","IVMRImageCompositor.TermCompositionTarget","IVMRImageCompositor::TermCompositionTarget","IVMRImageCompositorStopCompositing","TermCompositionTarget","TermCompositionTarget method [DirectShow]","TermCompositionTarget method [DirectShow]","IVMRImageCompositor interface","dshow.ivmrimagecompositor_termcompositiontarget","strmif/IVMRImageCompositor::TermCompositionTarget"]
old-location: dshow\ivmrimagecompositor_termcompositiontarget.htm
tech.root: dshow
ms.assetid: a9526be0-06aa-4fe3-ba05-fbac01806ec4
ms.date: 4/26/2023
ms.keywords: IVMRImageCompositor interface [DirectShow],TermCompositionTarget method, IVMRImageCompositor.TermCompositionTarget, IVMRImageCompositor::TermCompositionTarget, IVMRImageCompositorStopCompositing, TermCompositionTarget, TermCompositionTarget method [DirectShow], TermCompositionTarget method [DirectShow],IVMRImageCompositor interface, dshow.ivmrimagecompositor_termcompositiontarget, strmif/IVMRImageCompositor::TermCompositionTarget
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
 - IVMRImageCompositor::TermCompositionTarget
 - strmif/IVMRImageCompositor::TermCompositionTarget
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
 - IVMRImageCompositor.TermCompositionTarget
---

# IVMRImageCompositor::TermCompositionTarget


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>TermCompositionTarget</code> method informs the compositor that the current composition target is being replaced. Compositors should perform any necessary cleanup of the composition target in this method.

## -parameters

### -param pD3DDevice [in]

Pointer to the <b>IUnknown</b> interface of the Direct3D device object.

### -param pddsRenderTarget [in]

Specifies the DirectDraw surface

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>