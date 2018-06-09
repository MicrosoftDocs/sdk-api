---
UID: NN:mmstream.IStreamSample
title: IStreamSample
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\istreamsample.htm
old-project: DirectShow
ms.assetid: 57818d7d-3290-46f7-a3fd-8585cdd64ec3
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IStreamSample, IStreamSample interface [DirectShow], IStreamSample interface [DirectShow],described, IStreamSampleInterface, dshow.istreamsample, mmstream/IStreamSample
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STREAM_STATE
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamSample interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IStreamSample</code> interface provides control over the behavior of stream samples. You can retrieve the media stream that created the sample, set or retrieve sample start and stop times, check the sample's completion status, and perform a developer-specified function on the sample itself.

Implement this interface when you implement a media stream for a new media type. The interface is exposed on sample objects created by media streams.

Use this interface when you want to control data samples created by <a href="https://msdn.microsoft.com/97f5dfdc-5941-4b58-a618-1c7e9f6665e1">IMediaStream</a> or its derived interfaces.

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
<a href="https://msdn.microsoft.com/bfc3fd16-20b1-4581-abb0-66781aa3d584">CompletionStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the current sample's latest asynchronous update. If the update isn't complete, you can force it to complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfc38480-7b8d-42ad-937b-dd39384796c9">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the media stream object that created the current sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8c716fe-6731-4b54-9b4b-3b0f896f176b">GetSampleTimes</a>
</td>
<td align="left" width="63%">
Retrieves the current sample's start and end times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8d21ea2-0104-44e1-9f5b-5c0c23593e43">SetSampleTimes</a>
</td>
<td align="left" width="63%">
Sets the current sample's start and end times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Performs a synchronous or an asynchronous update on the current sample.

</td>
</tr>
</table> 

