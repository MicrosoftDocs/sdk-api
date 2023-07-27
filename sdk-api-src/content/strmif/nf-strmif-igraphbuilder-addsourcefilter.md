---
UID: NF:strmif.IGraphBuilder.AddSourceFilter
title: IGraphBuilder::AddSourceFilter (strmif.h)
description: The AddSourceFilter method adds a source filter for a specified file to the filter graph.
helpviewer_keywords: ["AddSourceFilter","AddSourceFilter method [DirectShow]","AddSourceFilter method [DirectShow]","IGraphBuilder interface","IGraphBuilder interface [DirectShow]","AddSourceFilter method","IGraphBuilder.AddSourceFilter","IGraphBuilder::AddSourceFilter","IGraphBuilderAddSourceFilter","dshow.igraphbuilder_addsourcefilter","strmif/IGraphBuilder::AddSourceFilter"]
old-location: dshow\igraphbuilder_addsourcefilter.htm
tech.root: dshow
ms.assetid: ed4d7fc6-558b-474f-ae8d-58aa8479b4d2
ms.date: 4/26/2023
ms.keywords: AddSourceFilter, AddSourceFilter method [DirectShow], AddSourceFilter method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],AddSourceFilter method, IGraphBuilder.AddSourceFilter, IGraphBuilder::AddSourceFilter, IGraphBuilderAddSourceFilter, dshow.igraphbuilder_addsourcefilter, strmif/IGraphBuilder::AddSourceFilter
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
 - IGraphBuilder::AddSourceFilter
 - strmif/IGraphBuilder::AddSourceFilter
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
 - IGraphBuilder.AddSourceFilter
---

# IGraphBuilder::AddSourceFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddSourceFilter</code> method adds a source filter for a specified file to the filter graph.

## -parameters

### -param lpcwstrFileName [in]

Specifies the name of the file to load.

### -param lpcwstrFilterName [in]

Specifies a name for the source filter.

### -param ppFilter [out]

Receives a pointer to the filter's <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The source filter does not support the <a href="/windows/desktop/api/strmif/nn-strmif-ifilesourcefilter">IFileSourceFilter</a> interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_LOAD_SOURCE_FILTER</b></dt>
</dl>
</td>
<td width="60%">
The source filter for this file could not be loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
File or object not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_UNKNOWN_FILE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type of this file was not recognized.

</td>
</tr>
</table>

## -remarks

This method searches for an installed filter that can read the specified file. If it finds one, the method adds it to the filter graph and returns a pointer to the filter's <b>IBaseFilter</b> interface. To determine the media type and compression scheme of the file, the Filter Graph Manager reads the first few bytes of the file, looking for specific patterns of bytes, as documented in the article <a href="/windows/desktop/DirectShow/registering-a-custom-file-type">Registering a Custom File Type</a>.

The application is responsible for building the rest of the filter graph. To do so, call <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-enumpins">IBaseFilter::EnumPins</a> to enumerate the output pins on the source filter. Then use either the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a> method or the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a> method.

If the method succeeds, the <b>IBaseFilter</b> interface has an outstanding reference count. The caller must release the interface.

To render a file for default playback, use the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a> method.

The Filter Graph Manager holds a reference count on the filter until the filter is removed from the graph or the Filter Graph Manager is released.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>