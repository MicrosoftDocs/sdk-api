---
UID: NN:amstream.IAMMediaTypeStream
title: IAMMediaTypeStream (amstream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iammediatypestream.htm
tech.root: DirectShow
ms.assetid: 6ca1bad2-625b-4415-8311-acd5443452c1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMediaTypeStream, IAMMediaTypeStream interface [DirectShow], IAMMediaTypeStream interface [DirectShow],described, IAMMediaTypeStreamInterface, amstream/IAMMediaTypeStream, dshow.iammediatypestream
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
 - IAMMediaTypeStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for creating multimedia streams with arbitrary media types. Use this interface if you need to create a multimedia stream with a format that is not supported by the other Microsoft DirectShow multimedia streaming interfaces.

<div class="alert"><b>Note</b>  For video streams, use the <a href="https://msdn.microsoft.com/en-us/library/Dd406806(v=VS.85).aspx">IDirectDrawMediaStream</a> interface instead of this interface. For audio streams, use the <a href="https://msdn.microsoft.com/en-us/library/Dd389516(v=VS.85).aspx">IAudioMediaStream</a> interface.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeStream</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd407041(v=VS.85).aspx">IMediaStream</a>. <b>IAMMediaTypeStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaTypeStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319683(v=VS.85).aspx">CreateSample</a>
</td>
<td align="left" width="63%">
Creates a stream sample and optionally specifies the sample buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319684(v=VS.85).aspx">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319685(v=VS.85).aspx">GetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Retrieves the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319686(v=VS.85).aspx">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the format of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319687(v=VS.85).aspx">SetStreamAllocatorRequirements</a>
</td>
<td align="left" width="63%">
Sets the allocator requirements for the stream. This method is not currently implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd407041(v=VS.85).aspx">IMediaStream</a>
 

 

