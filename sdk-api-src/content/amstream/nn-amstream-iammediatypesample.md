---
UID: NN:amstream.IAMMediaTypeSample
title: IAMMediaTypeSample
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iammediatypesample.htm
tech.root: DirectShow
ms.assetid: e0a62251-68ee-4318-b09a-0aac6b73bf54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMediaTypeSample, IAMMediaTypeSample interface [DirectShow], IAMMediaTypeSample interface [DirectShow],described, IAMMediaTypeSampleInterface, amstream/IAMMediaTypeSample, dshow.iammediatypesample
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
 - IAMMediaTypeSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
This interface contains methods for manipulating stream samples with arbitrary media types. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd319683(v=VS.85).aspx">IAMMediaTypeStream::CreateSample</a> method to create a sample that exposes this interface.

The methods in this interface parallel those of the <a href="https://msdn.microsoft.com/en-us/library/Dd407001(v=VS.85).aspx">IMediaSample</a> interface, although <b>IAMMediaTypeSample</b> contains a <a href="https://msdn.microsoft.com/en-us/library/Dd319678(v=VS.85).aspx">SetPointer</a> method in addition to the <a href="https://msdn.microsoft.com/en-us/library/Dd319668(v=VS.85).aspx">GetPointer</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeSample</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd377143(v=VS.85).aspx">IStreamSample</a>. <b>IAMMediaTypeSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMMediaTypeSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319664(v=VS.85).aspx">GetActualDataLength</a>
</td>
<td align="left" width="63%">
Retrieves the data length of the sample, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319665(v=VS.85).aspx">GetMediaTime</a>
</td>
<td align="left" width="63%">
Retrieves the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319667(v=VS.85).aspx">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319668(v=VS.85).aspx">GetPointer</a>
</td>
<td align="left" width="63%">
Retrieves a read/write pointer to the buffer's memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319669(v=VS.85).aspx">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer data area, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319670(v=VS.85).aspx">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the stream times at which this sample should start and stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319671(v=VS.85).aspx">IsDiscontinuity</a>
</td>
<td align="left" width="63%">
Determines if this sample represents a discontinuity in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319672(v=VS.85).aspx">IsPreroll</a>
</td>
<td align="left" width="63%">
Determines if this sample is part of the preroll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319673(v=VS.85).aspx">IsSyncPoint</a>
</td>
<td align="left" width="63%">
Determines if the beginning of a sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319674(v=VS.85).aspx">SetActualDataLength</a>
</td>
<td align="left" width="63%">
Sets the sample's data length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319675(v=VS.85).aspx">SetDiscontinuity</a>
</td>
<td align="left" width="63%">
Sets the discontinuity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319676(v=VS.85).aspx">SetMediaTime</a>
</td>
<td align="left" width="63%">
Sets the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319677(v=VS.85).aspx">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319678(v=VS.85).aspx">SetPointer</a>
</td>
<td align="left" width="63%">
Sets the pointer to the media sample's memory buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319679(v=VS.85).aspx">SetPreroll</a>
</td>
<td align="left" width="63%">
Specifies whether this is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319680(v=VS.85).aspx">SetSyncPoint</a>
</td>
<td align="left" width="63%">
Specifies whether the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd319681(v=VS.85).aspx">SetTime</a>
</td>
<td align="left" width="63%">
Sets the stream times at which this sample should start and stop.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd377143(v=VS.85).aspx">IStreamSample</a>
 

 

