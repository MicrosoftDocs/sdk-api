---
UID: NF:strmif.IGraphBuilder.RenderFile
title: IGraphBuilder::RenderFile
author: windows-sdk-content
description: The RenderFile method builds a filter graph that renders the specified file.
old-location: dshow\igraphbuilder_renderfile.htm
old-project: DirectShow
ms.assetid: 449aec08-c03e-41d6-8c04-0e871e532d11
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IGraphBuilder interface [DirectShow],RenderFile method, IGraphBuilder.RenderFile, IGraphBuilder::RenderFile, IGraphBuilderRenderFile, RenderFile, RenderFile method [DirectShow], RenderFile method [DirectShow],IGraphBuilder interface, dshow.igraphbuilder_renderfile, strmif/IGraphBuilder::RenderFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphBuilder::RenderFile


## -description



The <code>RenderFile</code> method builds a filter graph that renders the specified file.




## -parameters




### -param lpcwstrFile




### -param lpcwstrPlayList






#### - lpwstrFile [in]

Specifies a wide-character string that contains the name of a media file.


#### - lpwstrPlayList [in]

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



If the <i>lpwstrFile</i> parameter specifies a media file, the method builds a filter graph for default playback. First it adds a source filter that can read the file, using the same process as the <a href="https://msdn.microsoft.com/ed4d7fc6-558b-474f-ae8d-58aa8479b4d2">IGraphBuilder::AddSourceFilter</a> method. Then it renders the output pins on the source filter, adding intermediate filters if necessary. It tries filters in the same order as the <a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">IGraphBuilder::Connect</a> method.

During the connection process, the Filter Graph Manager ignores pins on intermediate filters if the pin name begins with a tilde (~). For more information, see <a href="https://msdn.microsoft.com/67a837f3-8b81-4651-a0fa-fed7b61e71c2">PIN_INFO</a>.

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
The following example downloads an AVI file over HTTP, using the <a href="https://msdn.microsoft.com/405fd6ea-aa17-4d11-8f07-067468cb090b">File Source (URL)</a> filter:

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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder Interface</a>
 

 

