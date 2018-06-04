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

# IDvbParentalRatingDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) parental rating descriptor. The parental rating descriptor appears in the DVB service information as part of the event information table (EIT) or selection information table (SIT) and includes a rating based on age. The descriptor may include extensions based on other rating criteria.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbParentalRatingDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbParentalRatingDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbParentalRatingDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72dcfb91-4137-4149-b30d-2551cb209688">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in a  DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/019c6998-74b3-4966-ad5d-b8da2bbacca5">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b439669-6458-46d3-882d-5f20f2f22f23">GetRecordRating</a>
</td>
<td align="left" width="63%">
Gets the rating code from a DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30689876-39be-44dd-a480-c660dcf3ddd1">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB parental rating descriptor.

</td>
</tr>
</table> 

