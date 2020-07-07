---
UID: NN:dvbsiparser.IDvbParentalRatingDescriptor
title: IDvbParentalRatingDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) parental rating descriptor.
helpviewer_keywords: ["IDvbParentalRatingDescriptor","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbParentalRatingDescriptor","mstv.idvbparentalratingdescriptor"]
old-location: mstv\idvbparentalratingdescriptor.htm
tech.root: mstv
ms.assetid: 667ef815-ef22-4dd1-9457-49af674b24ab
ms.date: 12/05/2018
ms.keywords: IDvbParentalRatingDescriptor, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies], IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbParentalRatingDescriptor, mstv.idvbparentalratingdescriptor
f1_keywords:
- dvbsiparser/IDvbParentalRatingDescriptor
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDvbParentalRatingDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbParentalRatingDescriptor interface


## -description


Implements methods that get data from a Digital Video Broadcast (DVB) parental rating descriptor. The parental rating descriptor appears in the DVB service information as part of the event information table (EIT) or selection information table (SIT) and includes a rating based on age. The descriptor may include extensions based on other rating criteria.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbParentalRatingDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbParentalRatingDescriptor</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in a  DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-getrecordrating">GetRecordRating</a>
</td>
<td align="left" width="63%">
Gets the rating code from a DVB parental rating descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB parental rating descriptor.

</td>
</tr>
</table> 

