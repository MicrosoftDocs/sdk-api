---
UID: NN:amstream.IMediaStreamFilter
title: IMediaStreamFilter
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IMediaStreamFilter interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.
old-location: dshow\imediastreamfilter.htm
tech.root: DirectShow
ms.assetid: 1ac4976b-7088-47ac-9689-58c143746f05
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMediaStreamFilter, IMediaStreamFilter interface [DirectShow], IMediaStreamFilter interface [DirectShow],described, IMediaStreamFilterInterface, amstream/IMediaStreamFilter, dshow.imediastreamfilter
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
 - IMediaStreamFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaStreamFilter interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMediaStreamFilter</code> interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaStreamFilter</b> interface inherits from <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a>. <b>IMediaStreamFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaStreamFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e4fdc28-3117-4b9d-a914-ddb70aa5125d">AddMediaStream</a>
</td>
<td align="left" width="63%">
Connects a media stream object to the underlying filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ceec4ead-e439-4206-ab30-ae37d15c5b44">EndOfStream</a>
</td>
<td align="left" width="63%">
Signals the end of a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f62abda-6192-4adb-985d-9bffe310b407">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30b5d8f7-e3ab-48e4-aefe-3b3e04aba638">Flush</a>
</td>
<td align="left" width="63%">
Notifies the filter that one of its pins has flushed data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933f83a3-600e-4897-b4df-a481d2874155">GetCurrentStreamTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27ef63cf-36a4-4d35-bd38-3c51b1343ee1">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ddbf0b-17aa-4481-81a7-6d4a12275c31">ReferenceTimeToStreamTime</a>
</td>
<td align="left" width="63%">
Converts a reference time to stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cb15898-8a22-4621-a6e5-bb5d17640749">SupportSeeking</a>
</td>
<td align="left" width="63%">
Initializes the filter to support seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5669a3c6-b060-49e8-b8e6-2e3617b44d62">WaitUntil</a>
</td>
<td align="left" width="63%">
Causes the filter to block until a specified stream time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a>
 

 

