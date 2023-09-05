---
UID: NF:control.IMediaControl.AddSourceFilter
title: IMediaControl::AddSourceFilter (control.h)
description: The AddSourceFilter method adds a source filter to the filter graph.
helpviewer_keywords: ["AddSourceFilter","AddSourceFilter method [DirectShow]","AddSourceFilter method [DirectShow]","IMediaControl interface","IMediaControl interface [DirectShow]","AddSourceFilter method","IMediaControl.AddSourceFilter","IMediaControl::AddSourceFilter","IMediaControlAddSourceFilter","control/IMediaControl::AddSourceFilter","dshow.imediacontrol_addsourcefilter"]
old-location: dshow\imediacontrol_addsourcefilter.htm
tech.root: dshow
ms.assetid: b0d59a47-23a7-4e59-adfa-e01945a5d014
ms.date: 4/26/2023
ms.keywords: AddSourceFilter, AddSourceFilter method [DirectShow], AddSourceFilter method [DirectShow],IMediaControl interface, IMediaControl interface [DirectShow],AddSourceFilter method, IMediaControl.AddSourceFilter, IMediaControl::AddSourceFilter, IMediaControlAddSourceFilter, control/IMediaControl::AddSourceFilter, dshow.imediacontrol_addsourcefilter
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
 - IMediaControl::AddSourceFilter
 - control/IMediaControl::AddSourceFilter
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
 - IMediaControl.AddSourceFilter
---

# IMediaControl::AddSourceFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddSourceFilter</code> method adds a source filter to the filter graph.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.AddSourceFilter</b> method. C++ applications should use the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-addsourcefilter">IGraphBuilder::AddSourceFilter</a> method instead.

## -parameters

### -param strFilename [in]

Specifies the name of the file to load.

### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IFilterInfo</b> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>