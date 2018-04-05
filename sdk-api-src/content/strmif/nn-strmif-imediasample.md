---
UID: NN:strmif.IMediaSample
title: IMediaSample
author: windows-driver-content
description: The IMediaSample interface sets and retrieves properties on media samples.
old-location: dshow\imediasample.htm
old-project: DirectShow
ms.assetid: 883e5e3b-db91-4806-96cc-c6f8cddfcca6
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IMediaSample, IMediaSample interface [DirectShow], IMediaSample interface [DirectShow], described, IMediaSampleInterface, dshow.imediasample, strmif/IMediaSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaSample
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample interface


## -description



The <code>IMediaSample</code> interface sets and retrieves properties on media samples. A media sample is a COM object that contains a block of media data. Media samples support the use of shared memory buffers among filters.

Typically, applications do not call methods on this interface. Filters use this interface to set properties on samples, and deliver the samples to a downstream filter. The downstream filter uses the interface to retrieve the properties and read the data. The filter can modify the data in place, or it can copy the sample, modify the copy, and pass the copy downstream.

The <a href="https://msdn.microsoft.com/638cb75d-9be6-4ba1-a116-47e2d62b689d">IMediaSample2</a> interface inherits this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMediaSample</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMediaSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMediaSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d89dbaef-01ff-4379-b696-cdd1a6a9801b">GetActualDataLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb2a8fd4-4a25-482c-8509-f43461c708d6">GetMediaTime</a>
</td>
<td align="left" width="63%">
Retrieves the media times for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abccec09-c5a0-4192-9bdf-9240d1b73357">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type, if the media type differs from the previous sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3c69dfb-6ee4-401b-8dcb-4e42a8cd8156">GetPointer</a>
</td>
<td align="left" width="63%">
Retrieves a read/write pointer to this buffer's memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dc50db2-dc75-4c04-ac30-78275ee35ce8">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5e95ef3-a101-41c4-8947-f099fcd2490e">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the stream times at which this sample should begin and finish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bab511e-a744-4b6e-afe3-0ceb473dfcae">IsDiscontinuity</a>
</td>
<td align="left" width="63%">
Determines if this sample represents a break in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7df1d34f-ba55-42bd-b61b-272ef72e13a8">IsPreroll</a>
</td>
<td align="left" width="63%">
Determines if this sample is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eed64bd9-1300-4db3-a3ed-c7e8ff9c7c8f">IsSyncPoint</a>
</td>
<td align="left" width="63%">
Determines if the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db8a768e-7550-4165-8f87-308ec7f2e07f">SetActualDataLength</a>
</td>
<td align="left" width="63%">
Sets the length of the valid data in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57041c71-4c7e-463a-92f5-c77a76aa545a">SetDiscontinuity</a>
</td>
<td align="left" width="63%">
Specifies whether this sample represents a break in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ae9db99-828d-4ac9-aa51-668b84d4dfab">SetMediaTime</a>
</td>
<td align="left" width="63%">
Sets the media times for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5be0997a-ae70-45fb-94e4-cb5e0a36d71a">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a92f2774-19ac-4630-ad66-2299336d1338">SetPreroll</a>
</td>
<td align="left" width="63%">
Specifies whether this sample is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2770045-c18b-4dbc-b104-873e07c0b5aa">SetSyncPoint</a>
</td>
<td align="left" width="63%">
Specifies whether the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/531eef13-8b04-48d2-9070-7f6e34cacd9e">SetTime</a>
</td>
<td align="left" width="63%">
Sets the stream time when this sample should begin and finish.

</td>
</tr>
</table> 

