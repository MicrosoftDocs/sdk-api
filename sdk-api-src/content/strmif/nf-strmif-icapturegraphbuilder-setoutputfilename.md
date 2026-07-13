---
UID: NF:strmif.ICaptureGraphBuilder.SetOutputFileName
title: ICaptureGraphBuilder::SetOutputFileName (strmif.h)
description: Note  The ICaptureGraphBuilder interface is deprecated. Use ICaptureGraphBuilder2 instead. Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.
helpviewer_keywords: ["ICaptureGraphBuilder interface [DirectShow]","SetOutputFileName method","ICaptureGraphBuilder.SetOutputFileName","ICaptureGraphBuilder::SetOutputFileName","ICaptureGraphBuilderSetOutputFileName","SetOutputFileName","SetOutputFileName method [DirectShow]","SetOutputFileName method [DirectShow]","ICaptureGraphBuilder interface","dshow.icapturegraphbuilder_setoutputfilename","strmif/ICaptureGraphBuilder::SetOutputFileName"]
old-location: dshow\icapturegraphbuilder_setoutputfilename.htm
tech.root: dshow
ms.assetid: f410465f-c560-49ab-9194-66d708274f77
ms.date: 4/26/2023
ms.keywords: ICaptureGraphBuilder interface [DirectShow],SetOutputFileName method, ICaptureGraphBuilder.SetOutputFileName, ICaptureGraphBuilder::SetOutputFileName, ICaptureGraphBuilderSetOutputFileName, SetOutputFileName, SetOutputFileName method [DirectShow], SetOutputFileName method [DirectShow],ICaptureGraphBuilder interface, dshow.icapturegraphbuilder_setoutputfilename, strmif/ICaptureGraphBuilder::SetOutputFileName
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Reference:\_Dshowh
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
req.dll: Quartz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICaptureGraphBuilder::SetOutputFileName
 - strmif/ICaptureGraphBuilder::SetOutputFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Quartz.dll
api_name:
 - ICaptureGraphBuilder.SetOutputFileName
---

# ICaptureGraphBuilder::SetOutputFileName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>ICaptureGraphBuilder</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2</a> instead.</div>
<div> </div>
Creates the rendering section of the filter graph, which will save bits to disk with the specified file name.

## -parameters

### -param pType [in]

Pointer to a <b>GUID</b> representing the media subtype. Must be <code>&amp;MEDIASUBTYPE_Avi</code>.

### -param lpstrFile [in]

Pointer to a wide-character string containing the output file name.

### -param ppf [out]

Address of a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface representing the multiplexer filter. This method increments the reference count on the <b>IBaseFilter</b> interface so you must decrement the reference count by using the <b>Release</b> method on this parameter when done using the filter.

### -param ppSink [out]

Address of a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter</a> interface representing the file writer. This method increments the reference count on the IFileSinkFilter interface so you must decrement the reference count using <b>Release</b> when done using the filter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. Audio-Video Interleaved (AVI) is the only supported output format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Instance of the AVI multiplexer filter was successfully created.

</td>
</tr>
</table>

## -remarks

This method inserts the multiplexer and the file writer into the filter graph and calls <a href="/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter-setfilename">IFileSinkFilter::SetFileName</a> to set the output file name.

You can use the <i>ppf</i> parameter returned by this method as the <i>pfRenderer</i> parameter in calls to <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder-renderstream">RenderStream</a>.

You can use the <i>pSink</i> parameter from this method in a call to <a href="/windows/desktop/api/strmif/nf-strmif-ifilesinkfilter-setfilename">SetFileName</a> to change the file name set by <code>ICaptureGraphBuilder::SetOutputFileName</code>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder">ICaptureGraphBuilder Interface</a>