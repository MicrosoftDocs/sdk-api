---
UID: NN:strmif.IFileSourceFilter
title: IFileSourceFilter (strmif.h)
description: The IFileSourceFilter interface is exposed by source filters to set the file name and media type of the media file that they are to render.
helpviewer_keywords: ["IFileSourceFilter","IFileSourceFilter interface [DirectShow]","IFileSourceFilter interface [DirectShow]","described","IFileSourceFilterInterface","dshow.ifilesourcefilter","strmif/IFileSourceFilter"]
old-location: dshow\ifilesourcefilter.htm
tech.root: dshow
ms.assetid: ad70fddb-4fc9-4010-a469-9a8ca4b47379
ms.date: 4/26/2023
ms.keywords: IFileSourceFilter, IFileSourceFilter interface [DirectShow], IFileSourceFilter interface [DirectShow],described, IFileSourceFilterInterface, dshow.ifilesourcefilter, strmif/IFileSourceFilter
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
 - IFileSourceFilter
 - strmif/IFileSourceFilter
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
 - IFileSourceFilter
---

# IFileSourceFilter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IFileSourceFilter</code> interface is exposed by source filters to set the file name and media type of the media file that they are to render. It is an abbreviated version of the COM <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> interface. If the file has a type that can be determined by the algorithm described in <a href="/windows/desktop/DirectShow/registering-a-custom-file-type">Registering a Custom File Type</a>, the recommended file source filter CLSID is used when the filter graph manager attempts to render the filter graph.

If a filter needs the name of a file to open, it should expose this interface to allow an application to set the file name. Note that there is no base class implementation of this interface.

An application that inserts file source filters directly must query for this interface and set the file name. Normally, the filter graph manager uses this interface when an application calls <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>. The Graphedt.exe tool queries for the <b>IFileSourceFilter</b> interface and prompts for a file name if it finds it.

## -inheritance

The <b>IFileSourceFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileSourceFilter</b> also has these types of members:

