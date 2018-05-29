---
UID: NN:dvbsiparser.IDvbParentalRatingDescriptor
title: IDvbParentalRatingDescriptor
author: windows-sdk-content
description: Implements methods that get data from a Digital Video Broadcast (DVB) parental rating descriptor.
old-location: mstv\idvbparentalratingdescriptor.htm
old-project: mstv
ms.assetid: 667ef815-ef22-4dd1-9457-49af674b24ab
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDvbParentalRatingDescriptor, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies], IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbParentalRatingDescriptor, mstv.idvbparentalratingdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbParentalRatingDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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

