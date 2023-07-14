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

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that enable the client to get information from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream. The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IPBDASiParser::GetEIT</a> method returns a pointer to this interface.

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

The <b>IPBDA_EIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDA_EIT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

