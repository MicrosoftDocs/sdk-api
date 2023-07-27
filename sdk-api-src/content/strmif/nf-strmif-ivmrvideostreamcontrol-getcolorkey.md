---
UID: NF:strmif.IVMRVideoStreamControl.GetColorKey
title: IVMRVideoStreamControl::GetColorKey (strmif.h)
description: The GetColorKey method retrieves the source color key currently set for this stream.
helpviewer_keywords: ["GetColorKey","GetColorKey method [DirectShow]","GetColorKey method [DirectShow]","IVMRVideoStreamControl interface","IVMRVideoStreamControl interface [DirectShow]","GetColorKey method","IVMRVideoStreamControl.GetColorKey","IVMRVideoStreamControl::GetColorKey","IVMRVideoStreamControlGetColorKey","dshow.ivmrvideostreamcontrol_getcolorkey","strmif/IVMRVideoStreamControl::GetColorKey"]
old-location: dshow\ivmrvideostreamcontrol_getcolorkey.htm
tech.root: dshow
ms.assetid: 2075ac12-c799-4716-994f-46ff6928e670
ms.date: 4/26/2023
ms.keywords: GetColorKey, GetColorKey method [DirectShow], GetColorKey method [DirectShow],IVMRVideoStreamControl interface, IVMRVideoStreamControl interface [DirectShow],GetColorKey method, IVMRVideoStreamControl.GetColorKey, IVMRVideoStreamControl::GetColorKey, IVMRVideoStreamControlGetColorKey, dshow.ivmrvideostreamcontrol_getcolorkey, strmif/IVMRVideoStreamControl::GetColorKey
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
 - IVMRVideoStreamControl::GetColorKey
 - strmif/IVMRVideoStreamControl::GetColorKey
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
 - IVMRVideoStreamControl.GetColorKey
---

# IVMRVideoStreamControl::GetColorKey


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetColorKey</code> method retrieves the source color key currently set for this stream.

## -parameters

### -param lpClrKey [out]

Address of a <a href="/windows/desktop/api/strmif/ns-strmif-ddcolorkey">DDCOLORKEY</a> structure that receives the source color key.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrvideostreamcontrol">IVMRVideoStreamControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey">IVMRVideoStreamControl::SetColorKey</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>