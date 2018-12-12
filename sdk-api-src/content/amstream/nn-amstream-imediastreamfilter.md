---
UID: NN:amstream.IMediaStreamFilter
title: IMediaStreamFilter
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IMediaStreamFilter interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.
old-location: dshow\imediastreamfilter.htm
tech.root: DirectShow
ms.assetid: 1ac4976b-7088-47ac-9689-58c143746f05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaStreamFilter, IMediaStreamFilter interface [DirectShow], IMediaStreamFilter interface [DirectShow],described, IMediaStreamFilterInterface, amstream/IMediaStreamFilter, dshow.imediastreamfilter
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaStreamFilter</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd389526(v=VS.85).aspx">IBaseFilter</a>. <b>IMediaStreamFilter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd407043(v=VS.85).aspx">AddMediaStream</a>
</td>
<td align="left" width="63%">
Connects a media stream object to the underlying filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407044(v=VS.85).aspx">EndOfStream</a>
</td>
<td align="left" width="63%">
Signals the end of a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407045(v=VS.85).aspx">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407046(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Notifies the filter that one of its pins has flushed data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407047(v=VS.85).aspx">GetCurrentStreamTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407048(v=VS.85).aspx">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407049(v=VS.85).aspx">ReferenceTimeToStreamTime</a>
</td>
<td align="left" width="63%">
Converts a reference time to stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407050(v=VS.85).aspx">SupportSeeking</a>
</td>
<td align="left" width="63%">
Initializes the filter to support seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd407051(v=VS.85).aspx">WaitUntil</a>
</td>
<td align="left" width="63%">
Causes the filter to block until a specified stream time.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd389526(v=VS.85).aspx">IBaseFilter</a>
 

 

