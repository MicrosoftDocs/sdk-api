---
UID: NF:strmif.IFileSourceFilter.Load
title: IFileSourceFilter::Load (strmif.h)
description: The Load method causes a source filter to load a media file.
helpviewer_keywords: ["IFileSourceFilter interface [DirectShow]","Load method","IFileSourceFilter.Load","IFileSourceFilter::Load","IFileSourceFilterLoad","Load","Load method [DirectShow]","Load method [DirectShow]","IFileSourceFilter interface","dshow.ifilesourcefilter_load","strmif/IFileSourceFilter::Load"]
old-location: dshow\ifilesourcefilter_load.htm
tech.root: dshow
ms.assetid: a44b8153-19d5-43ad-936c-214c694eeeb6
ms.date: 4/26/2023
ms.keywords: IFileSourceFilter interface [DirectShow],Load method, IFileSourceFilter.Load, IFileSourceFilter::Load, IFileSourceFilterLoad, Load, Load method [DirectShow], Load method [DirectShow],IFileSourceFilter interface, dshow.ifilesourcefilter_load, strmif/IFileSourceFilter::Load
req.header: strmif.h
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
 - IFileSourceFilter::Load
 - strmif/IFileSourceFilter::Load
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
 - IFileSourceFilter.Load
---

# IFileSourceFilter::Load


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Load</code> method causes a source filter to load a media file.

## -parameters

### -param pszFileName [in]

Pointer to the name of the file to open.

### -param pmt [in]

Pointer to the media type of the file. This can be <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method initializes the interface. It is not designed to load multiple files, and any calls to this method after the first call will fail.

For the <a href="/windows/desktop/DirectShow/file-source--async--filter">File Source (Async)</a> filter, <i>pszFileName</i> specifies the absolute path name of a local file. For the <a href="/windows/desktop/DirectShow/file-source--url--filter">File Source (URL)</a> filter, <i>pszFileName</i> specifies the URL of a file to download. For other filter implementations, <i>pszFileName</i> might require a file name or a URL, depending on the filter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilesourcefilter">IFileSourceFilter Interface</a>