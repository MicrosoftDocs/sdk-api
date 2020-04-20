---
UID: NF:strmif.IGraphBuilder.RenderFile
title: IGraphBuilder::RenderFile (strmif.h)
description: The RenderFile method builds a filter graph that renders the specified file.helpviewer_keywords: ["IGraphBuilder interface [DirectShow]","RenderFile method","IGraphBuilder.RenderFile","IGraphBuilder::RenderFile","IGraphBuilderRenderFile","RenderFile","RenderFile method [DirectShow]","RenderFile method [DirectShow]","IGraphBuilder interface","dshow.igraphbuilder_renderfile","strmif/IGraphBuilder::RenderFile"]
old-location: dshow\igraphbuilder_renderfile.htm
tech.root: DirectShow
ms.assetid: 449aec08-c03e-41d6-8c04-0e871e532d11
ms.date: 12/05/2018
ms.keywords: IGraphBuilder interface [DirectShow],RenderFile method, IGraphBuilder.RenderFile, IGraphBuilder::RenderFile, IGraphBuilderRenderFile, RenderFile, RenderFile method [DirectShow], RenderFile method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_renderfile, strmif/IGraphBuilder::RenderFile
f1_keywords:
- strmif/IGraphBuilder.RenderFile
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IGraphBuilder.RenderFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphBuilder::RenderFile


## -description



The <code>RenderFile</code> method builds a filter graph that renders the specified file.




## -parameters




### -param lpcwstrFile [in]

Specifies a wide-character string that contains the name of a media file.


### -param lpcwstrPlayList [in]

Reserved. Must be <b>NULL</b>.


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
<dt><b>VFW_S_AUDIO_NOT_RENDERED</b></dt>
</dl>
</td>
<td width="60%">
Partial success; the audio was not rendered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Success; the Filter Graph Manager modified the filter name to avoid duplication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_PARTIAL_RENDER</b></dt>
</dl>
</td>
<td width="60%">
Some of the streams in this movie are in an unsupported format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_VIDEO_NOT_RENDERED</b></dt>
</dl>
</td>
<td width="60%">
Partial success; some of the streams in this movie are in an unsupported format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Operation aborted.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

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
<dt><b>VFW_E_CANNOT_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
No combination of intermediate filters could be found to make the connection.

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
<dt><b>VFW_E_CANNOT_RENDER</b></dt>
</dl>
</td>
<td width="60%">
No combination of filters could be found to render the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_INVALID_FILE_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The file format is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An object or name was not found.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_UNSUPPORTED_STREAM</b></dt>
</dl>
</td>
<td width="60%">
Cannot play back the file: the format is not supported.

</td>
</tr>
</table>
 




## -remarks



If the <i>lpwstrFile</i> parameter specifies a media file, the method builds a filter graph for default playback. First it adds a source filter that can read the file, using the same process as the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-addsourcefilter">IGraphBuilder::AddSourceFilter</a> method. Then it renders the output pins on the source filter, adding intermediate filters if necessary. It tries filters in the same order as the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a> method.

During the connection process, the Filter Graph Manager ignores pins on intermediate filters if the pin name begins with a tilde (~). For more information, see [PIN_INFO](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-pin_info).

Note that the <code>RenderFile</code> method does not remove any filters from the graph. If you call <code>RenderFile</code> twice, the second call simply adds more filters to the graph. When you run the graph, both sources will play at the same time.


#### Examples

The following example renders an AVI file for default playback:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
hr = pGraph-&gt;RenderFile(L"C:\\Media\\Example.avi", 0);
</pre>
</td>
</tr>
</table></span></div>
The following example downloads an AVI file over HTTP, using the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/file-source--url--filter">File Source (URL)</a> filter:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
hr = pGraph-&gt;RenderFile(L"http://example.microsoft.com/Example.avi", 0);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder Interface</a>
 

 

