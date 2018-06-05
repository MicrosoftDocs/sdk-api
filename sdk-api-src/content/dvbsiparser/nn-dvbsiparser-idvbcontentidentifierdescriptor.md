---
UID: NN:dvbsiparser.IDvbContentIdentifierDescriptor
title: IDvbContentIdentifierDescriptor
author: windows-sdk-content
description: Implements methods that get information from a Digital Video Broadcast (DVB) content identifier descriptor.
old-location: mstv\idvbcontentidentifierdescriptor.htm
old-project: mstv
ms.assetid: bdd15b6f-2f1e-438a-a2fd-f3fa4df2a9fd
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDvbContentIdentifierDescriptor, IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies], IDvbContentIdentifierDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbContentIdentifierDescriptor, mstv.idvbcontentidentifierdescriptor
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbContentIdentifierDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbContentIdentifierDescriptor interface


## -description


Implements methods that get information from a Digital Video Broadcast (DVB) content identifier descriptor.  Content identifier descriptors uniquely identify a unit of content in a DVB broadcast stream. Content identifier descriptors appear in the DVB service information as part of the event information table (EIT), which provides information about the events in each service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbContentIdentifierDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbContentIdentifierDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/cd96a052-52e6-4de7-aa44-66c2caa4d5f5">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records in a DVB  content identifier descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0138416a-70d6-4a64-957b-8b0eb031b589">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a DVB  content identifier descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de3593a6-f39c-4c4a-9ddf-1343186d98e3">GetRecordCrid</a>
</td>
<td align="left" width="63%">
Gets the content reference identifier (CRID) from a DVB content identifier descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ab8dbe8-ddb8-4c24-a830-c770eab2b23f">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for a DVB content identifier descriptor.

</td>
</tr>
</table> 

