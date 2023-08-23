---
UID: NF:strmif.IFilterGraph.FindFilterByName
title: IFilterGraph::FindFilterByName (strmif.h)
description: The FindFilterByName method finds a filter that was added to the filter graph with a specific name.
helpviewer_keywords: ["FindFilterByName","FindFilterByName method [DirectShow]","FindFilterByName method [DirectShow]","IFilterGraph interface","IFilterGraph interface [DirectShow]","FindFilterByName method","IFilterGraph.FindFilterByName","IFilterGraph::FindFilterByName","IFilterGraphFindFilterByName","dshow.ifiltergraph_findfilterbyname","strmif/IFilterGraph::FindFilterByName"]
old-location: dshow\ifiltergraph_findfilterbyname.htm
tech.root: dshow
ms.assetid: 59d90274-ac00-4e19-bcee-2282e26994b5
ms.date: 4/26/2023
ms.keywords: FindFilterByName, FindFilterByName method [DirectShow], FindFilterByName method [DirectShow],IFilterGraph interface, IFilterGraph interface [DirectShow],FindFilterByName method, IFilterGraph.FindFilterByName, IFilterGraph::FindFilterByName, IFilterGraphFindFilterByName, dshow.ifiltergraph_findfilterbyname, strmif/IFilterGraph::FindFilterByName
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
 - IFilterGraph::FindFilterByName
 - strmif/IFilterGraph::FindFilterByName
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
 - IFilterGraph.FindFilterByName
---

# IFilterGraph::FindFilterByName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>FindFilterByName</code> method finds a filter that was added to the filter graph with a specific name.

## -parameters

### -param pName [in]

[in, string] Pointer to the name to search for.

### -param ppFilter [out]

Receives a pointer to the filter's <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface. The caller must release the interface.

## -returns

Returns one of the following values.

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
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No filter was found with the specified name.

</td>
</tr>
</table>

## -remarks

If no filter is found, the method returns a <b>NULL</b> pointer in the <i>ppFilter</i> parameter.

The returned <b>IBaseFilter</b> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph">IFilterGraph Interface</a>