---
UID: NN:amstream.IMediaStreamFilter
title: IMediaStreamFilter (amstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The IMediaStreamFilter interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.
old-location: dshow\imediastreamfilter.htm
tech.root: DirectShow
ms.assetid: 1ac4976b-7088-47ac-9689-58c143746f05
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMediaStreamFilter, IMediaStreamFilter interface [DirectShow], IMediaStreamFilter interface [DirectShow],described, IMediaStreamFilterInterface, amstream/IMediaStreamFilter, dshow.imediastreamfilter
ms.topic: interface
f1_keywords: 
 - "amstream/IMediaStreamFilter"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaStreamFilter interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IMediaStreamFilter</code> interface is supported by the Media Stream filter, which is used internally by the multimedia stream object. Applications should not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaStreamFilter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>. <b>IMediaStreamFilter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-addmediastream">AddMediaStream</a>
</td>
<td align="left" width="63%">
Connects a media stream object to the underlying filter graph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-endofstream">EndOfStream</a>
</td>
<td align="left" width="63%">
Signals the end of a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-enummediastreams">EnumMediaStreams</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-flush">Flush</a>
</td>
<td align="left" width="63%">
Notifies the filter that one of its pins has flushed data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-getcurrentstreamtime">GetCurrentStreamTime</a>
</td>
<td align="left" width="63%">
Retrieves the current stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-getmediastream">GetMediaStream</a>
</td>
<td align="left" width="63%">
Retrieves a media stream, specified by purpose ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-referencetimetostreamtime">ReferenceTimeToStreamTime</a>
</td>
<td align="left" width="63%">
Converts a reference time to stream time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-supportseeking">SupportSeeking</a>
</td>
<td align="left" width="63%">
Initializes the filter to support seeking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nf-amstream-imediastreamfilter-waituntil">WaitUntil</a>
</td>
<td align="left" width="63%">
Causes the filter to block until a specified stream time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a>
 

 

