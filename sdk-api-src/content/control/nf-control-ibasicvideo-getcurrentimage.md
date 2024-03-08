---
UID: NF:control.IBasicVideo.GetCurrentImage
title: IBasicVideo::GetCurrentImage (control.h)
description: The GetCurrentImage method retrieves the current image waiting at the renderer.
helpviewer_keywords: ["GetCurrentImage","GetCurrentImage method [DirectShow]","GetCurrentImage method [DirectShow]","IBasicVideo interface","IBasicVideo interface [DirectShow]","GetCurrentImage method","IBasicVideo.GetCurrentImage","IBasicVideo::GetCurrentImage","IBasicVideoGetCurrentImage","control/IBasicVideo::GetCurrentImage","dshow.ibasicvideo_getcurrentimage"]
old-location: dshow\ibasicvideo_getcurrentimage.htm
tech.root: dshow
ms.assetid: 3e7fbf27-3519-4c02-b785-98e29902df65
ms.date: 4/26/2023
ms.keywords: GetCurrentImage, GetCurrentImage method [DirectShow], GetCurrentImage method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetCurrentImage method, IBasicVideo.GetCurrentImage, IBasicVideo::GetCurrentImage, IBasicVideoGetCurrentImage, control/IBasicVideo::GetCurrentImage, dshow.ibasicvideo_getcurrentimage
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IBasicVideo::GetCurrentImage
 - control/IBasicVideo::GetCurrentImage
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
 - IBasicVideo.GetCurrentImage
---

# IBasicVideo::GetCurrentImage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentImage</code> method retrieves the current image waiting at the renderer.

## -parameters

### -param pBufferSize [in, out]

Pointer to a variable that contains the size of the buffer that the caller is passing in. If <i>pDIBImage</i> is <b>NULL</b>, this parameter receives the required buffer size.

### -param pDIBImage [out]

Pointer to a buffer where the complete image will be stored in device-independent bitmap (DIB) format. Cast the pointer to a long pointer type.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and the Video Mixing Renderer (VMR) implement this method differently.

<h3><a id="Video_Renderer_only_"></a><a id="video_renderer_only_"></a><a id="VIDEO_RENDERER_ONLY_"></a>Video Renderer only:</h3>
This method fails if the renderer is using DirectDraw acceleration. Unfortunately, this depends on the end-user's hardware configuration, so in practice this method is not reliable.

Pause the Video Renderer before calling this method. Otherwise, the method returns VFW_E_NOT_PAUSED. Make sure that the pause operation has completed by calling <a href="/windows/desktop/api/control/nf-control-imediacontrol-getstate">IMediaControl::GetState</a>; if the pause operation has not completed, the <b>GetCurrentImage</b> method returns E_UNEXPECTED. Depending on what data the source filter has available, the video renderer is not guaranteed to service this request. If no image is available, it returns E_FAIL.

<h3><a id="Video_Mixing_Renderer_only_"></a><a id="video_mixing_renderer_only_"></a><a id="VIDEO_MIXING_RENDERER_ONLY_"></a>Video Mixing Renderer only:</h3>
This method is reliable regardless of whether the VMR is using DirectDraw acceleration and regardless of the current graph state (running, stopped, or paused).


<h3><a id="Video_Renderer_and_Video_Mixing_Renderer_"></a><a id="video_renderer_and_video_mixing_renderer_"></a><a id="VIDEO_RENDERER_AND_VIDEO_MIXING_RENDERER_"></a>Video Renderer and Video Mixing Renderer:</h3>
To obtain the required buffer size to hold the image, call this method with a <b>NULL</b> pointer in the <i>pDIBImage</i> parameter. The method returns the required buffer size in the <i>pBufferSize</i> parameter. Allocate a buffer of that size and call the method again, with <i>pDIBImage</i> pointing to the buffer. On the second call, use <i>pBufferSize</i> to specify the buffer size. If the buffer is too small to hold the complete image, the method returns E_OUTOFMEMORY. 


If the method succeeds, the buffer is filled with the entire DIB image, including the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, plus any palette entries and bit masks as defined in the Win32 <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure. The format of the image depends on the type provided by the source filter, and cannot be specified in advance.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>