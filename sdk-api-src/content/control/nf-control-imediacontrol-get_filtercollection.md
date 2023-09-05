---
UID: NF:control.IMediaControl.get_FilterCollection
title: IMediaControl::get_FilterCollection (control.h)
description: The get_FilterCollection method retrieves a collection of the filters in the filter graph.
helpviewer_keywords: ["IMediaControl interface [DirectShow]","get_FilterCollection method","IMediaControl.get_FilterCollection","IMediaControl::get_FilterCollection","IMediaControlget_FilterCollection","control/IMediaControl::get_FilterCollection","dshow.imediacontrol_get_filtercollection","get_FilterCollection","get_FilterCollection method [DirectShow]","get_FilterCollection method [DirectShow]","IMediaControl interface"]
old-location: dshow\imediacontrol_get_filtercollection.htm
tech.root: dshow
ms.assetid: 9a14e971-365e-4061-8d07-01216e793864
ms.date: 4/26/2023
ms.keywords: IMediaControl interface [DirectShow],get_FilterCollection method, IMediaControl.get_FilterCollection, IMediaControl::get_FilterCollection, IMediaControlget_FilterCollection, control/IMediaControl::get_FilterCollection, dshow.imediacontrol_get_filtercollection, get_FilterCollection, get_FilterCollection method [DirectShow], get_FilterCollection method [DirectShow],IMediaControl interface
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
 - IMediaControl::get_FilterCollection
 - control/IMediaControl::get_FilterCollection
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
 - IMediaControl.get_FilterCollection
---

# IMediaControl::get_FilterCollection


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_FilterCollection</code> method retrieves a collection of the filters in the filter graph.



This method is intended for use by Visual Basic 6.0 applications. It was documented for Visual Basic 6.0 as the <b>FilgraphManager.FilterCollection</b> property. C++ applications should use the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-enumfilters">IFilterGraph::EnumFilters</a> method instead.

## -parameters

### -param ppUnk [out]

Receives a pointer to the <b>IDispatch</b> interface.  The caller must release the interface. You can query the returned pointer for the <b>IAMCollection</b> interface. The collection contains a list of <b>IFilterInfo</b> pointers.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/control/nn-control-imediacontrol">IMediaControl Interface</a>