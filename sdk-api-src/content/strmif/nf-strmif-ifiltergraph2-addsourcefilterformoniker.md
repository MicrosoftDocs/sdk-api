---
UID: NF:strmif.IFilterGraph2.AddSourceFilterForMoniker
title: IFilterGraph2::AddSourceFilterForMoniker (strmif.h)
description: The AddSourceFilterForMoniker method creates a source filter from an IMoniker pointer and adds the filter to the graph.
helpviewer_keywords: ["AddSourceFilterForMoniker","AddSourceFilterForMoniker method [DirectShow]","AddSourceFilterForMoniker method [DirectShow]","IFilterGraph2 interface","IFilterGraph2 interface [DirectShow]","AddSourceFilterForMoniker method","IFilterGraph2.AddSourceFilterForMoniker","IFilterGraph2::AddSourceFilterForMoniker","IFilterGraph2AddSourceFilterForMoniker","dshow.ifiltergraph2_addsourcefilterformoniker","strmif/IFilterGraph2::AddSourceFilterForMoniker"]
old-location: dshow\ifiltergraph2_addsourcefilterformoniker.htm
tech.root: dshow
ms.assetid: 7e398df6-7cb7-4028-be34-3040a2cd1c2b
ms.date: 4/26/2023
ms.keywords: AddSourceFilterForMoniker, AddSourceFilterForMoniker method [DirectShow], AddSourceFilterForMoniker method [DirectShow],IFilterGraph2 interface, IFilterGraph2 interface [DirectShow],AddSourceFilterForMoniker method, IFilterGraph2.AddSourceFilterForMoniker, IFilterGraph2::AddSourceFilterForMoniker, IFilterGraph2AddSourceFilterForMoniker, dshow.ifiltergraph2_addsourcefilterformoniker, strmif/IFilterGraph2::AddSourceFilterForMoniker
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
 - IFilterGraph2::AddSourceFilterForMoniker
 - strmif/IFilterGraph2::AddSourceFilterForMoniker
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
 - IFilterGraph2.AddSourceFilterForMoniker
---

# IFilterGraph2::AddSourceFilterForMoniker


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>AddSourceFilterForMoniker</code> method creates a source filter from an <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> pointer and adds the filter to the graph. For example, you can obtain a moniker for a system device, such as a video capture device, and add a video capture filter for that device. (For more information about system device monikers, see the <a href="/windows/desktop/api/strmif/nn-strmif-icreatedevenum">ICreateDevEnum</a> interface.)

## -parameters

### -param pMoniker [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface.

### -param pCtx [in]

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> bind context interface.

### -param lpcwstrFilterName [in]

Name for the filter.

### -param ppFilter [out]

Receives a pointer to the source filter's <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> pointer. The caller must release the interface.

## -returns

Returns and <b>HRESULT</b> value. Possible values include the following.

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
Success; but the specified name was a duplicate, so the Filter Graph Manager modified the name.

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
<dt><b>VFW_E_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Failed to add a filter with a duplicate name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CANNOT_LOAD_SOURCE_FILTER</b></dt>
</dl>
</td>
<td width="60%">
The source filter for could not be loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_UNKNOWN_FILE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type of this file is not recognized.

</td>
</tr>
</table>

## -remarks

The Filter Graph Manager holds a reference count on the filter until the filter is removed from the graph or the Filter Graph Manager is released.


#### Examples

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IBaseFilter *pSource = NULL;
IMoniker *pMoniker = NULL;

// Use IEnumMonikers to get the IMoniker pointer. (Not shown.)

// Create a bind context for working with the moniker.
IBindCtx *pContext=0;
hr = CreateBindCtx(0, &amp;pContext);
if (SUCCEEDED(hr))
{
    // Query the Filter Graph Manager for IFilterGraph2.
    IFilterGraph2 *pFG2 = NULL;
    hr = pGraph-&gt;QueryInterface(IID_IFilterGraph2, (void**)&amp;pFG2);
    if (SUCCEEDED(hr))
    {
        // Create the source filter.
        hr = pFG2-&gt;AddSourceFilterForMoniker(pMoniker, pContext,
                 L"Source", &amp;pSource);
        pFG2-&gt;Release();
    }
    pContext-&gt;Release();
}
pMoniker-&gt;Release();
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltergraph2">IFilterGraph2 Interface</a>