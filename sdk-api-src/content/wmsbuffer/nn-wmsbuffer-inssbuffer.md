---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# INSSBuffer interface


## -description



The <b>INSSBuffer</b> interface is the basic interface of a buffer object. A buffer object is a wrapper around a memory buffer. The methods exposed by this interface are used to manipulate the buffer.

In both writing and reading ASF files, buffer objects are used to contain samples. Depending upon where you use a sample, you will obtain a reference to the <b>INSSBuffer</b> interface in one of three ways:

<ul>
<li>When passing samples to the writer, you can obtain buffer objects by calling <a href="https://msdn.microsoft.com/b23b2364-fb36-479f-bf92-76a5bb4722de">IWMWriter::AllocateSample</a>.</li>
<li>When you are receiving samples from the asynchronous reader, buffer objects are created automatically, and references to an <b>INSSBuffer</b> interface are passed with every call the reader makes to the <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">IWMReaderCallback::OnSample</a> callback method.</li>
<li>When you are receiving samples from the synchronous reader, a reference to an <b>INSSBuffer</b> interface is set with every call you make to <a href="https://msdn.microsoft.com/948047b3-3b87-4381-9320-c9602716ade2">IWMSyncReader::GetNextSample</a>.</li>
</ul>


The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/74d174a1-ede8-482c-ae42-19ca65c6cad4">INSSBuffer2</a>
</td>
<td>IID_INSSBuffer2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3ebf80d0-b5b0-4024-805d-e0a3855574bf">INSSBuffer3</a>
</td>
<td>IID_INSSBuffer3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/d6531e52-b58b-46ed-a47b-444cd98e1ec5">INSSBuffer4</a>
</td>
<td>IID_INSSBuffer4</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INSSBuffer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INSSBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INSSBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Retrieves the location of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb03d006-fbaa-4971-8022-41a7fa29fb87">GetBufferAndLength</a>
</td>
<td align="left" width="63%">
Retrieves the location and size of the used portion of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a964124d-f25b-442c-a29d-0ee595bdbcce">GetLength</a>
</td>
<td align="left" width="63%">
Retrieves the size of the used portion of the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b386c24-1737-4e30-98fa-444fc8a34503">GetMaxLength</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size to which a buffer can be set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0e8d8a-efc7-4f1b-8a42-7907439ed8af">SetLength</a>
</td>
<td align="left" width="63%">
Specifies the size of the used portion of the buffer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0812261c-698c-4071-929c-4363a16dd5a8">Buffer Object</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/e0aabe05-b317-42ac-85fc-5a75165722d4">Reading ASF Files</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

