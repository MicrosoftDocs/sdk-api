---
UID: NF:strmif.IFilterMapper.RegisterFilter
title: IFilterMapper::RegisterFilter (strmif.h)
description: Note  The IFilterMapper interface is deprecated. Use IFilterMapper2 instead. Adds a filter to the registry; the filter can then be enumerated.
helpviewer_keywords: ["IFilterMapper interface [DirectShow]","RegisterFilter method","IFilterMapper.RegisterFilter","IFilterMapper::RegisterFilter","IFilterMapperRegisterFilter","RegisterFilter","RegisterFilter method [DirectShow]","RegisterFilter method [DirectShow]","IFilterMapper interface","dshow.ifiltermapper_registerfilter","strmif/IFilterMapper::RegisterFilter"]
old-location: dshow\ifiltermapper_registerfilter.htm
tech.root: dshow
ms.assetid: e21da510-f4e6-417e-978d-bb53bf78cf94
ms.date: 4/26/2023
ms.keywords: IFilterMapper interface [DirectShow],RegisterFilter method, IFilterMapper.RegisterFilter, IFilterMapper::RegisterFilter, IFilterMapperRegisterFilter, RegisterFilter, RegisterFilter method [DirectShow], RegisterFilter method [DirectShow],IFilterMapper interface, dshow.ifiltermapper_registerfilter, strmif/IFilterMapper::RegisterFilter
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper::RegisterFilter
 - strmif/IFilterMapper::RegisterFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IFilterMapper.RegisterFilter
---

# IFilterMapper::RegisterFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IFilterMapper</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2</a> instead.</div>
<div> </div>
Adds a filter to the registry; the filter can then be enumerated.

## -parameters

### -param clsid [in]

Globally unique identifier (<b>GUID</b>) of the filter.

### -param Name [in]

Descriptive name for the filter.

### -param dwMerit [in]

Position in the order of enumeration. Filters with higher merit are enumerated first.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The merit (as defined by the <i>dwMerit</i> parameter) controls the order in which the filter graph manager tries filters when performing an operation as a result of a call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>. The filter graph manager finds all filters registered with the correct media type and then tries the one with the highest merit, using other criteria in the registration to choose between filters with equal merit.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper">IFilterMapper Interface</a>