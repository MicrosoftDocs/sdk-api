---
UID: NN:amstream.IAMMultiMediaStream
title: IAMMultiMediaStream
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.
old-location: dshow\iammultimediastream.htm
old-project: DirectShow
ms.assetid: 2f604156-68ef-4770-9929-6dbfd46c4d6d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMMultiMediaStream, IAMMultiMediaStream interface [DirectShow], IAMMultiMediaStream interface [DirectShow],described, IAMMultiMediaStreamInterface, amstream/IAMMultiMediaStream, dshow.iammultimediastream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: AMSI_RESULT
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
req.lib: 
req.dll: 
req.irql: 
---

# IAMMultiMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMultiMediaStream</code> interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMultiMediaStream</b> interface inherits from <a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream</a>. <b>IAMMultiMediaStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3ccfb776-6a4e-48da-857d-6693cf916c40">AddMediaStream</a>
</td>
<td align="left" width="63%">
Adds the specified media stream to the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e4df9cb-4008-4615-a179-ae1e76c22337">GetFilter</a>
</td>
<td align="left" width="63%">
Retrieves the specified filter from the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e772ced-d14e-45da-9e97-36579e7e3ffd">GetFilterGraph</a>
</td>
<td align="left" width="63%">
Retrieves the associated filter graph's <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Sets the stream type. If the <i>pFilterGraph</i> parameter is non-<b>NULL</b> the filter graph passed in is used for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b3f7401-9afe-41e5-827f-e4e8d60b7480">OpenFile</a>
</td>
<td align="left" width="63%">
Opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccfed197-6637-4283-9996-56049da49b84">OpenMoniker</a>
</td>
<td align="left" width="63%">
Opens a file or device moniker; you can read media data from this moniker if DirectShow supports the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09866cf0-650d-4d8e-81d4-6a568709c027">Render</a>
</td>
<td align="left" width="63%">
Renders the current filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream</a>
 

 

