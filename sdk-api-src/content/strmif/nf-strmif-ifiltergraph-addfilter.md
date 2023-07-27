---
UID: NF:strmif.IFilterGraph.AddFilter
title: IFilterGraph::AddFilter (strmif.h)
description: The AddFilter method adds a filter to the graph.
helpviewer_keywords: ["AddFilter","AddFilter method [DirectShow]","AddFilter method [DirectShow]","IFilterGraph interface","IFilterGraph interface [DirectShow]","AddFilter method","IFilterGraph.AddFilter","IFilterGraph::AddFilter","IFilterGraphAddFilter","dshow.ifiltergraph_addfilter","strmif/IFilterGraph::AddFilter"]
old-location: dshow\ifiltergraph_addfilter.htm
tech.root: dshow
ms.assetid: 8f837917-015f-427f-b234-b0ccbcf943eb
ms.date: 4/26/2023
ms.keywords: AddFilter, AddFilter method [DirectShow], AddFilter method [DirectShow],IFilterGraph interface, IFilterGraph interface [DirectShow],AddFilter method, IFilterGraph.AddFilter, IFilterGraph::AddFilter, IFilterGraphAddFilter, dshow.ifiltergraph_addfilter, strmif/IFilterGraph::AddFilter
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
 - IFilterGraph::AddFilter
 - strmif/IFilterGraph::AddFilter
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
 - IFilterGraph.AddFilter
---

# IFilterGraph::AddFilter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddFilter</code> method adds a filter to the graph.

## -parameters

### -param pFilter [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter to add.

### -param pName [in]

Pointer to a wide-character string containing a name for filter.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>VFW_S_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Successfully added a filter with a duplicate name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

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
<dt><b>VFW_E_CERTIFICATION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Use of this filter is restricted by a software key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Failed to add a filter with a duplicate name.

</td>
</tr>
</table>

## -remarks

The name of the filter can be <b>NULL</b>, in which case the Filter Graph Manager generates a name. If the name is not <b>NULL</b> and is not unique, this method will modify the name in an attempt to generate a new unique name. If this is successful, this method returns VFW_S_DUPLICATE_NAME. If it cannot generate a unique name, it returns VFW_E_DUPLICATE_NAME.

<code>AddFilter</code> calls the filter's <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-joinfiltergraph">IBaseFilter::JoinFilterGraph</a> method to inform the filter that it has been added. <code>AddFilter</code> must be called before attempting to use the <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ifiltergraph-connectdirect">IFilterGraph::ConnectDirect</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a> method to connect or render pins belonging to the added filter.

The Filter Graph Manager holds a reference count on the filter until the filter is removed from the graph or the Filter Graph Manager is released.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>