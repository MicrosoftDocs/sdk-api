---
UID: NN:amstream.IAMMultiMediaStream
title: IAMMultiMediaStream (amstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.
old-location: dshow\iammultimediastream.htm
tech.root: DirectShow
ms.assetid: 2f604156-68ef-4770-9929-6dbfd46c4d6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMMultiMediaStream, IAMMultiMediaStream interface [DirectShow], IAMMultiMediaStream interface [DirectShow],described, IAMMultiMediaStreamInterface, amstream/IAMMultiMediaStream, dshow.iammultimediastream
ms.topic: interface
f1_keywords: ["amstream/IAMMultiMediaStream"]
req.header: amstream.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMultiMediaStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMultiMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMultiMediaStream</code> interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMultiMediaStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream</a>. <b>IAMMultiMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMultiMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-addmediastream">AddMediaStream</a>
</td>
<td align="left" width="63%">
Adds the specified media stream to the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-getfilter">GetFilter</a>
</td>
<td align="left" width="63%">
Retrieves the specified filter from the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-getfiltergraph">GetFilterGraph</a>
</td>
<td align="left" width="63%">
Retrieves the associated filter graph's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Sets the stream type. If the <i>pFilterGraph</i> parameter is non-<b>NULL</b> the filter graph passed in is used for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-openfile">OpenFile</a>
</td>
<td align="left" width="63%">
Opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-openmoniker">OpenMoniker</a>
</td>
<td align="left" width="63%">
Opens a file or device moniker; you can read media data from this moniker if DirectShow supports the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-iammultimediastream-render">Render</a>
</td>
<td align="left" width="63%">
Renders the current filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream</a>
 

 

