---
UID: NN:dvbsiparser.IPBDA_EIT
title: IPBDA_EIT (dvbsiparser.h)
description: Implements methods that enable the client to get information from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream. The IPBDASiParser::GetEIT method returns a pointer to this interface.
helpviewer_keywords: ["IPBDA_EIT","IPBDA_EIT interface [Microsoft TV Technologies]","IPBDA_EIT interface [Microsoft TV Technologies]","described","dvbsiparser/IPBDA_EIT","mstv.ipbda_eit"]
old-location: mstv\ipbda_eit.htm
tech.root: mstv
ms.assetid: cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56
ms.date: 12/05/2018
ms.keywords: IPBDA_EIT, IPBDA_EIT interface [Microsoft TV Technologies], IPBDA_EIT interface [Microsoft TV Technologies],described, dvbsiparser/IPBDA_EIT, mstv.ipbda_eit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPBDA_EIT
 - dvbsiparser/IPBDA_EIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT
---

# IPBDA_EIT interface


## -description

Implements methods that enable the client to get information from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IPBDASiParser::GetEIT</a> method returns a pointer to this interface.

An EIT provides information about events in each service, such as the event name, the start time, and the duration. An EIT can hold information about the transport stream that carries it, or it can hold information about other transport streams. There are two types of EITs:
<ul>
<li>Present/Following EITs contain information about the current event and the next chronological event. This type of EIT can be used to create a simple UI at the receiver.</li>
<li>Schedule EITs contain a list of events that occur after the next event. This type of event can be used to create an electronic program guide.</li>
</ul>EIT sections are given the following table identifiers.
<table>
<tr>
<th>Table identifier</th>
<th>Description</th>
</tr>
<tr>
<td>0x80</td>
<td>Present/Following EIT for this transport stream.</td>
</tr>
<tr>
<td>0x81</td>
<td>Schedule EIT for this transport stream. </td>
</tr>
</table>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDA_EIT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDA_EIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDA_EIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of  event records in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Get the number of descriptors associated with an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694801(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Gets an event record descriptor from the EIT based on the record's position in the descriptor list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets an event record descriptor from the EIT based on the record's identifying tag.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecordduration">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Gets the event duration from an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecordeventid">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Gets the identifier from an  event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecordstarttime">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Gets the event start time from an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getserviceidx">GetServiceIdx</a>
</td>
<td align="left" width="63%">
Gets the service identifier from the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-gettableid">GetTableId</a>
</td>
<td align="left" width="63%">
Gets the table identifier from the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.


</td>
</tr>
</table>

