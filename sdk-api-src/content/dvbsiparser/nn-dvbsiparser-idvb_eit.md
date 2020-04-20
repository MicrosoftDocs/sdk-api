---
UID: NN:dvbsiparser.IDVB_EIT
title: IDVB_EIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["IDVB_EIT","IDVB_EIT interface [Microsoft TV Technologies]","IDVB_EIT interface [Microsoft TV Technologies]","described","IDVB_EITInterface","dvbsiparser/IDVB_EIT","mstv.idvb_eit"]
old-location: mstv\idvb_eit.htm
tech.root: mstv
ms.assetid: 86280e1e-09c3-45a4-bdfb-53eda8e5700e
ms.date: 12/05/2018
ms.keywords: IDVB_EIT, IDVB_EIT interface [Microsoft TV Technologies], IDVB_EIT interface [Microsoft TV Technologies],described, IDVB_EITInterface, dvbsiparser/IDVB_EIT, mstv.idvb_eit
f1_keywords:
- dvbsiparser/IDVB_EIT
dev_langs:
- c++
req.header: dvbsiparser.h
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
- dvbsiparser.h
api_name:
- IDVB_EIT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>IDVB_EIT</b> interface enables the client to get information from a DVB event information table (EIT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IDvbSiParser::GetEIT</a> method returns a pointer to this interface.

An EIT provides information about events in each service, such as the event name, the start time, and the duration. An EIT can hold information about the transport stream that carries it, or it can hold information about other transport streams. There are two types of EITs:
<ul>
<li><i>Present/following</i> EITs contain information about the current event and the next chronological event. This type of EIT can be used to create a simple user interface at the receiver.</li>
<li><i>Schedule</i> EITs contain a list of events that occur after the next event. This type of event can be used to create an electronic program guide (EPG).</li>
</ul>EIT sections are given the following table identifiers (TIDs).
<table>
<tr>
<th>TID</th>
<th>Description</th>
</tr>
<tr>
<td>0x4E</td>
<td>Present/following EIT for this transport stream.</td>
</tr>
<tr>
<td>0x4F</td>
<td>Present/following EIT for another transport stream. </td>
</tr>
<tr>
<td>0x50 – 0x5F</td>
<td>Schedule EIT for this transport stream.</td>
</tr>
<tr>
<td>0x60 – 0x6F</td>
<td>Schedule EIT for another transport stream.</td>
</tr>
</table> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_EIT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_EIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_EIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-convertnexttocurrent">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getlasttableid">GetLastTableId</a>
</td>
<td align="left" width="63%">
Returns the last table identifier used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getnexttable">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd389801(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the EIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordduration">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Returns the event duration for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordeventid">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordfreecamode">GetRecordFreeCAMode</a>
</td>
<td align="left" width="63%">
Queries whether any of the component streams for an event are scrambled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordrunningstatus">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status of a particular event in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getrecordstarttime">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Returns the event start time for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getsegmentlastsectionnumber">GetSegmentLastSectionNumber</a>
</td>
<td align="left" width="63%">
Returns the section number of the last section in the subtable that contains this section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getserviceid">GetServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-registerfornexttable">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-registerforwhencurrent">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

