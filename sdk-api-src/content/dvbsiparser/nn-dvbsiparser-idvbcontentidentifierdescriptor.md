---
UID: NN:dvbsiparser.IDvbContentIdentifierDescriptor
title: IDvbContentIdentifierDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get information from a Digital Video Broadcast (DVB) content identifier descriptor.
old-location: mstv\idvbcontentidentifierdescriptor.htm
tech.root: mstv
ms.assetid: bdd15b6f-2f1e-438a-a2fd-f3fa4df2a9fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbContentIdentifierDescriptor, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies], IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbContentIdentifierDescriptor, mstv.idvbcontentidentifierdescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbContentIdentifierDescriptor"
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
 - IDvbContentIdentifierDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbContentIdentifierDescriptor interface


## -description


Implements methods that get information from a Digital Video Broadcast (DVB) content identifier descriptor.  Content identifier descriptors uniquely identify a unit of content in a DVB broadcast stream. Content identifier descriptors appear in the DVB service information as part of the event information table (EIT), which provides information about the events in each service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbContentIdentifierDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbContentIdentifierDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbContentIdentifierDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a DVB  content identifier descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB  content identifier descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-getrecordcrid">GetRecordCrid</a>
</td>
<td align="left" width="63%">
Gets the content reference identifier (CRID) from a DVB content identifier descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentidentifierdescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for a DVB content identifier descriptor.

</td>
</tr>
</table> 

