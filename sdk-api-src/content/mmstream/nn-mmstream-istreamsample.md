---
UID: NN:mmstream.IStreamSample
title: IStreamSample (mmstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\istreamsample.htm
tech.root: DirectShow
ms.assetid: 57818d7d-3290-46f7-a3fd-8585cdd64ec3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamSample, IStreamSample interface [DirectShow], IStreamSample interface [DirectShow],described, IStreamSampleInterface, dshow.istreamsample, mmstream/IStreamSample
ms.topic: interface
req.header: mmstream.h
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
 - mmstream.h
api_name:
 - IStreamSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamSample interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IStreamSample</code> interface provides control over the behavior of stream samples. You can retrieve the media stream that created the sample, set or retrieve sample start and stop times, check the sample's completion status, and perform a developer-specified function on the sample itself.

Implement this interface when you implement a media stream for a new media type. The interface is exposed on sample objects created by media streams.

Use this interface when you want to control data samples created by <a href="https://msdn.microsoft.com/en-us/library/Dd407041(v=VS.85).aspx">IMediaStream</a> or its derived interfaces.

In addition to the methods inherited from <b>IUnknown</b>, the <code>IStreamSample</code> interface exposes the following methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamSample</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377144(v=VS.85).aspx">CompletionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the current sample's latest asynchronous update. If the update isn't complete, you can force it to complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377145(v=VS.85).aspx">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the media stream object that created the current sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377146(v=VS.85).aspx">GetSampleTimes</a>
</td>
<td align="left" width="63%">
Retrieves the current sample's start and end times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377147(v=VS.85).aspx">SetSampleTimes</a>
</td>
<td align="left" width="63%">
Sets the current sample's start and end times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd377148(v=VS.85).aspx">Update</a>
</td>
<td align="left" width="63%">
Performs a synchronous or an asynchronous update on the current sample.

</td>
</tr>
</table> 

