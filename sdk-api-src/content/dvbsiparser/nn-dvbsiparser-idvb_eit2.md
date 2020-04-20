---
UID: NN:dvbsiparser.IDVB_EIT2
title: IDVB_EIT2 (dvbsiparser.h)
description: The IDVB_EIT2 interface enables an application to get information from a Digital Video Broadcasting (DVB) event information table (EIT). The IDvbSiParser2::GetEIT2 method returns a pointer to this interface. This interface extends the IDVB_EIT interface.helpviewer_keywords: ["IDVB_EIT2","IDVB_EIT2 interface [Microsoft TV Technologies]","IDVB_EIT2 interface [Microsoft TV Technologies]","described","dvbsiparser/IDVB_EIT2","mstv.idvb_eit2"]
old-location: mstv\idvb_eit2.htm
tech.root: mstv
ms.assetid: 9d93130c-12fb-4c76-98c1-cdfae113cf2c
ms.date: 12/05/2018
ms.keywords: IDVB_EIT2, IDVB_EIT2 interface [Microsoft TV Technologies], IDVB_EIT2 interface [Microsoft TV Technologies],described, dvbsiparser/IDVB_EIT2, mstv.idvb_eit2
f1_keywords:
- dvbsiparser/IDVB_EIT2
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
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
- IDVB_EIT2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT2 interface


## -description


The <b>IDVB_EIT2</b> interface enables an application to get information from a Digital Video Broadcasting (DVB) event information table (EIT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IDvbSiParser2::GetEIT2</a> method returns a pointer to this interface. This interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT</a> interface.

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
<td>0x50  – 0x5F</td>
<td>Schedule EIT for this transport stream.</td>
</tr>
<tr>
<td>0x60  – 0x6F</td>
<td>Schedule EIT for another transport stream.</td>
</tr>
</table> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_EIT2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT</a>. <b>IDVB_EIT2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_EIT2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit2-getrecordsection">GetRecordSection</a>
</td>
<td align="left" width="63%">
Gets the number of a section that contains an  EIT record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-registerforwhencurrent">GetSegmentInfo</a>
</td>
<td align="left" width="63%">
Gets data from a segment within an EIT record.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT</a>
 

 

