---
UID: NF:strmif.IFilterMapper2.UnregisterFilter
title: IFilterMapper2::UnregisterFilter (strmif.h)
description: The UnregisterFilter method removes filter information from the registry.
helpviewer_keywords: ["IFilterMapper2 interface [DirectShow]","UnregisterFilter method","IFilterMapper2.UnregisterFilter","IFilterMapper2::UnregisterFilter","IFilterMapper2UnregisterFilter","UnregisterFilter","UnregisterFilter method [DirectShow]","UnregisterFilter method [DirectShow]","IFilterMapper2 interface","dshow.ifiltermapper2_unregisterfilter","strmif/IFilterMapper2::UnregisterFilter"]
old-location: dshow\ifiltermapper2_unregisterfilter.htm
tech.root: dshow
ms.assetid: cfba764d-ec94-49a2-9aaf-2b107b742f83
ms.date: 4/26/2023
ms.keywords: IFilterMapper2 interface [DirectShow],UnregisterFilter method, IFilterMapper2.UnregisterFilter, IFilterMapper2::UnregisterFilter, IFilterMapper2UnregisterFilter, UnregisterFilter, UnregisterFilter method [DirectShow], UnregisterFilter method [DirectShow],IFilterMapper2 interface, dshow.ifiltermapper2_unregisterfilter, strmif/IFilterMapper2::UnregisterFilter
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
 - IFilterMapper2::UnregisterFilter
 - strmif/IFilterMapper2::UnregisterFilter
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
 - IFilterMapper2.UnregisterFilter
---

# IFilterMapper2::UnregisterFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnregisterFilter</code> method removes filter information from the registry.

## -parameters

### -param pclsidCategory [in]

Address of a GUID that specifies the filter category from which to remove the filter. For a list of categories, see <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.

### -param szInstance [in]

Instance data used to construct the device moniker's display name. Use the value that was originally passed to the <b>RegisterFilter</b> method.

### -param Filter [in]

Class identifier (CLSID) of the filter.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

If the filter was not registered, the method might return an error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2 Interface</a>