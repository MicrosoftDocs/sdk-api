---
UID: NF:strmif.IDecimateVideoImage.ResetDecimationImageSize
title: IDecimateVideoImage::ResetDecimationImageSize (strmif.h)
description: The ResetDecimationImageSize method specifies that the decoder should no longer decimate its output image.
helpviewer_keywords: ["IDecimateVideoImage interface [DirectShow]","ResetDecimationImageSize method","IDecimateVideoImage.ResetDecimationImageSize","IDecimateVideoImage::ResetDecimationImageSize","IDecimateVideoImageResetDecimationImageSize","ResetDecimationImageSize","ResetDecimationImageSize method [DirectShow]","ResetDecimationImageSize method [DirectShow]","IDecimateVideoImage interface","dshow.idecimatevideoimage_resetdecimationimagesize","strmif/IDecimateVideoImage::ResetDecimationImageSize"]
old-location: dshow\idecimatevideoimage_resetdecimationimagesize.htm
tech.root: dshow
ms.assetid: cae80d57-d04a-4835-bb45-2198f36c0539
ms.date: 4/26/2023
ms.keywords: IDecimateVideoImage interface [DirectShow],ResetDecimationImageSize method, IDecimateVideoImage.ResetDecimationImageSize, IDecimateVideoImage::ResetDecimationImageSize, IDecimateVideoImageResetDecimationImageSize, ResetDecimationImageSize, ResetDecimationImageSize method [DirectShow], ResetDecimationImageSize method [DirectShow],IDecimateVideoImage interface, dshow.idecimatevideoimage_resetdecimationimagesize, strmif/IDecimateVideoImage::ResetDecimationImageSize
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IDecimateVideoImage::ResetDecimationImageSize
 - strmif/IDecimateVideoImage::ResetDecimationImageSize
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
 - IDecimateVideoImage.ResetDecimationImageSize
---

# IDecimateVideoImage::ResetDecimationImageSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ResetDecimationImageSize</code> method specifies that the decoder should no longer decimate its output image.



## -returns

Returns an <b>HRESULT</b> value indicating the success or failure of the call.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idecimatevideoimage">IDecimateVideoImage Interface</a>
