---
UID: NN:amstream.IAMMultiMediaStream
title: IAMMultiMediaStream (amstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.
old-location: dshow\iammultimediastream.htm
tech.root: DirectShow
ms.assetid: 2f604156-68ef-4770-9929-6dbfd46c4d6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMultiMediaStream, IAMMultiMediaStream interface [DirectShow], IAMMultiMediaStream interface [DirectShow],described, IAMMultiMediaStreamInterface, amstream/IAMMultiMediaStream, dshow.iammultimediastream
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
---

# IAMMultiMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAMMultiMediaStream</code> interface is supported by the multimedia stream object. It contains methods for creating the underlying filter graph that the object manages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMultiMediaStream</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd390325(v=VS.85).aspx">IMultiMediaStream</a>. <b>IAMMultiMediaStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd319689(v=VS.85).aspx">AddMediaStream</a>
</td>
<td align="left" width="63%">
Adds the specified media stream to the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319690(v=VS.85).aspx">GetFilter</a>
</td>
<td align="left" width="63%">
Retrieves the specified filter from the current filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319691(v=VS.85).aspx">GetFilterGraph</a>
</td>
<td align="left" width="63%">
Retrieves the associated filter graph's <a href="https://msdn.microsoft.com/en-us/library/Dd390085(v=VS.85).aspx">IGraphBuilder</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319692(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Sets the stream type. If the <i>pFilterGraph</i> parameter is non-<b>NULL</b> the filter graph passed in is used for the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319693(v=VS.85).aspx">OpenFile</a>
</td>
<td align="left" width="63%">
Opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319694(v=VS.85).aspx">OpenMoniker</a>
</td>
<td align="left" width="63%">
Opens a file or device moniker; you can read media data from this moniker if DirectShow supports the media type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319695(v=VS.85).aspx">Render</a>
</td>
<td align="left" width="63%">
Renders the current filter graph.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd390325(v=VS.85).aspx">IMultiMediaStream</a>
 

 

