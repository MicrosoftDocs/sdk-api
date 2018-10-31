---
UID: NF:strmif.IGraphBuilder.AddSourceFilter
title: IGraphBuilder::AddSourceFilter
author: windows-sdk-content
description: The AddSourceFilter method adds a source filter for a specified file to the filter graph.
old-location: dshow\igraphbuilder_addsourcefilter.htm
tech.root: DirectShow
ms.assetid: ed4d7fc6-558b-474f-ae8d-58aa8479b4d2
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddSourceFilter, AddSourceFilter method [DirectShow], AddSourceFilter method [DirectShow],IGraphBuilder interface, IGraphBuilder interface [DirectShow],AddSourceFilter method, IGraphBuilder.AddSourceFilter, IGraphBuilder::AddSourceFilter, IGraphBuilderAddSourceFilter, dshow.igraphbuilder_addsourcefilter, strmif/IGraphBuilder::AddSourceFilter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IGraphBuilder.AddSourceFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphBuilder::AddSourceFilter


## -description



The <code>AddSourceFilter</code> method adds a source filter for a specified file to the filter graph.




## -parameters




### -param lpcwstrFileName

TBD


### -param lpcwstrFilterName

TBD


### -param ppFilter [out]

Receives a pointer to the filter's <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface. The caller must release the interface.


#### - lpwstrFileName [in]

Specifies the name of the file to load.


#### - lpwstrFilterName [in]

Specifies a name for the source filter.


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
The source filter does not support the <a href="https://msdn.microsoft.com/ad70fddb-4fc9-4010-a469-9a8ca4b47379">IFileSourceFilter</a> interface.

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



This method searches for an installed filter that can read the specified file. If it finds one, the method adds it to the filter graph and returns a pointer to the filter's <b>IBaseFilter</b> interface. To determine the media type and compression scheme of the file, the Filter Graph Manager reads the first few bytes of the file, looking for specific patterns of bytes, as documented in the article <a href="https://msdn.microsoft.com/bc0d5719-6325-40fe-8261-ad00b91f272c">Registering a Custom File Type</a>.

The application is responsible for building the rest of the filter graph. To do so, call <a href="https://msdn.microsoft.com/02675c93-7901-40f6-a9fc-f6f13f56acca">IBaseFilter::EnumPins</a> to enumerate the output pins on the source filter. Then use either the <a href="https://msdn.microsoft.com/8ddcbb73-8220-4d70-9ab3-58d99fa8a958">IGraphBuilder::Connect</a> method or the <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a> method.

If the method succeeds, the <b>IBaseFilter</b> interface has an outstanding reference count. The caller must release the interface.

To render a file for default playback, use the <a href="https://msdn.microsoft.com/449aec08-c03e-41d6-8c04-0e871e532d11">IGraphBuilder::RenderFile</a> method.

The Filter Graph Manager holds a reference count on the filter until the filter is removed from the graph or the Filter Graph Manager is released.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder Interface</a>
 

 

