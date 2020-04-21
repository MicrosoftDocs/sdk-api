---
UID: NN:dvbsiparser.IDvbLogicalChannel2Descriptor
title: IDvbLogicalChannel2Descriptor (dvbsiparser.h)
description: Implements methods that get data from a logical channel descriptor (LCD) in a Digital Video Broadcast (DVB) MPEG-2 stream that uses the format defined in the Nordig specification used in Scandinavian countries.helpviewer_keywords: ["IDvbLogicalChannel2Descriptor","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbLogicalChannel2Descriptor","mstv.idvblogicalchannel2descriptor"]
old-location: mstv\idvblogicalchannel2descriptor.htm
tech.root: mstv
ms.assetid: dc60db7f-ae49-48dd-bd8a-62899e5ca7a3
ms.date: 12/05/2018
ms.keywords: IDvbLogicalChannel2Descriptor, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies], IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbLogicalChannel2Descriptor, mstv.idvblogicalchannel2descriptor
f1_keywords:
- dvbsiparser/IDvbLogicalChannel2Descriptor
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
- IDvbLogicalChannel2Descriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbLogicalChannel2Descriptor interface


## -description


Implements methods that  get data from a logical channel descriptor (LCD) in a Digital Video Broadcast (DVB) MPEG-2 stream that uses the format defined in the Nordig specification used in Scandinavian countries.

 The logical channel descriptor may be present in the network information table (NIT).

By default, all methods in the base interface <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a> act on the first item in a list.  Once any  call to a <b>IDvbLogicalChannel2Descriptor</b> method completes successfully, the item that the method returns remains selected so that subsequent calls to <b>IDvbLogicalChannelDescriptor</b> methods act on the selected item.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbLogicalChannel2Descriptor</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor2</a>. <b>IDvbLogicalChannel2Descriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbLogicalChannel2Descriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getcountoflists">GetCountOfLists</a>
</td>
<td align="left" width="63%">
Gets the number of channel lists from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">GetListCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in a channel list from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountrycode">GetListCountryCode</a>
</td>
<td align="left" width="63%">
Gets the country code for a channel list from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistid">GetListId</a>
</td>
<td align="left" width="63%">
Gets a channel list identifier from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistnamew">GetListNameW</a>
</td>
<td align="left" width="63%">
Gets a country list name  from a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistrecordlogicalchannelnumber">GetListRecordLogicalChannelNumber</a>
</td>
<td align="left" width="63%">
Gets a logical channel number from a channel list in a logical channel descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistrecordserviceid">GetListRecordServiceId</a>
</td>
<td align="left" width="63%">
Gets a service identifier from a logical channel descriptor.

</td>
</tr>
</table> 

