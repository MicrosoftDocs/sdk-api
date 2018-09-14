---
UID: NN:amstream.IAMMediaTypeSample
title: IAMMediaTypeSample
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iammediatypesample.htm
tech.root: DirectShow
ms.assetid: e0a62251-68ee-4318-b09a-0aac6b73bf54
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMMediaTypeSample, IAMMediaTypeSample interface [DirectShow], IAMMediaTypeSample interface [DirectShow],described, IAMMediaTypeSampleInterface, amstream/IAMMediaTypeSample, dshow.iammediatypesample
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
This interface contains methods for manipulating stream samples with arbitrary media types. Call the <a href="https://msdn.microsoft.com/5bfdbf82-c298-498d-84e4-cd4d8cd13f82">IAMMediaTypeStream::CreateSample</a> method to create a sample that exposes this interface.

The methods in this interface parallel those of the <a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample</a> interface, although <b>IAMMediaTypeSample</b> contains a <a href="https://msdn.microsoft.com/fc7a04c5-3542-41e0-8abc-bb7b40bff2c9">SetPointer</a> method in addition to the <a href="https://msdn.microsoft.com/e1ca46d8-51d6-4dd5-bbcc-463acf53420c">GetPointer</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMMediaTypeSample</b> interface inherits from <a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample</a>. <b>IAMMediaTypeSample</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e73672c7-7400-40dd-be65-f6c30c476c91">GetActualDataLength</a>
</td>
<td align="left" width="63%">
Retrieves the data length of the sample, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed66c17-f18b-4c8b-b31a-6dd4f5ab4292">GetMediaTime</a>
</td>
<td align="left" width="63%">
Retrieves the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40a2640e-aaeb-44f2-a772-2deda2fd3999">GetMediaType</a>
</td>
<td align="left" width="63%">
Retrieves the media type of the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ca46d8-51d6-4dd5-bbcc-463acf53420c">GetPointer</a>
</td>
<td align="left" width="63%">
Retrieves a read/write pointer to the buffer's memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57dd7ec9-7615-42c5-9da7-44c4d71535c4">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the buffer data area, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffbbc857-ddcc-4625-b591-b95a256d40ba">GetTime</a>
</td>
<td align="left" width="63%">
Retrieves the stream times at which this sample should start and stop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/857729d9-ef46-461b-a3b5-bce9acb84538">IsDiscontinuity</a>
</td>
<td align="left" width="63%">
Determines if this sample represents a discontinuity in the data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57ae9d67-65b9-458e-ad94-f5d5c89d1984">IsPreroll</a>
</td>
<td align="left" width="63%">
Determines if this sample is part of the preroll.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0494f51e-2602-4574-88dd-0839a1d2f04f">IsSyncPoint</a>
</td>
<td align="left" width="63%">
Determines if the beginning of a sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/158a1761-7d42-4611-9667-9e717b23a2da">SetActualDataLength</a>
</td>
<td align="left" width="63%">
Sets the sample's data length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dcac2ce-c9a0-40be-aa86-b4acbd4d06a7">SetDiscontinuity</a>
</td>
<td align="left" width="63%">
Sets the discontinuity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d255840f-9ff5-4eb0-b3b4-1295d77403f8">SetMediaTime</a>
</td>
<td align="left" width="63%">
Sets the media time stamps for this sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13c065b4-9a46-42bd-aef9-dd2a87a355df">SetMediaType</a>
</td>
<td align="left" width="63%">
Sets the media type for the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc7a04c5-3542-41e0-8abc-bb7b40bff2c9">SetPointer</a>
</td>
<td align="left" width="63%">
Sets the pointer to the media sample's memory buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4815f4f-b919-497a-922e-b4d0d2078e4b">SetPreroll</a>
</td>
<td align="left" width="63%">
Specifies whether this is a preroll sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2ff9b33-c49c-4715-b580-f05670a0f405">SetSyncPoint</a>
</td>
<td align="left" width="63%">
Specifies whether the beginning of this sample is a synchronization point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8f2c1bd-ea78-43b8-881c-d1f1a64ee575">SetTime</a>
</td>
<td align="left" width="63%">
Sets the stream times at which this sample should start and stop.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample</a>
 

 

