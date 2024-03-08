---
UID: NN:dvbsiparser.IDVB_EIT
title: IDVB_EIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_EIT","IDVB_EIT interface [Microsoft TV Technologies]","IDVB_EIT interface [Microsoft TV Technologies]","described","IDVB_EITInterface","dvbsiparser/IDVB_EIT","mstv.idvb_eit"]
old-location: mstv\idvb_eit.htm
tech.root: mstv
ms.assetid: 86280e1e-09c3-45a4-bdfb-53eda8e5700e
ms.date: 12/05/2018
ms.keywords: IDVB_EIT, IDVB_EIT interface [Microsoft TV Technologies], IDVB_EIT interface [Microsoft TV Technologies],described, IDVB_EITInterface, dvbsiparser/IDVB_EIT, mstv.idvb_eit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDVB_EIT
 - dvbsiparser/IDVB_EIT
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
 - IDVB_EIT
---

# IDVB_EIT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>IDVB_EIT</b> interface enables the client to get information from a DVB event information table (EIT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IDvbSiParser::GetEIT</a> method returns a pointer to this interface.

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

The <b>IDVB_EIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_EIT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
