---
UID: NN:dvbsiparser.IPBDA_Services
title: IPBDA_Services (dvbsiparser.h)
description: Implements methods that initialize or retrieve Protected Broadcast Driver Architecture (PBDA) service records from a Program and System Information Protocol (PSIP) table in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["IPBDA_Services","IPBDA_Services interface [Microsoft TV Technologies]","IPBDA_Services interface [Microsoft TV Technologies]","described","dvbsiparser/IPBDA_Services","mstv.ipbda_services"]
old-location: mstv\ipbda_services.htm
tech.root: mstv
ms.assetid: 8d2d62cd-9f62-45d3-8b98-74bb8863c6d6
ms.date: 12/05/2018
ms.keywords: IPBDA_Services, IPBDA_Services interface [Microsoft TV Technologies], IPBDA_Services interface [Microsoft TV Technologies],described, dvbsiparser/IPBDA_Services, mstv.ipbda_services
f1_keywords:
- dvbsiparser/IPBDA_Services
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
req.idl: Dvbsiparser.idl
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
- IPBDA_Services
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_Services interface


## -description


Implements methods that initialize or retrieve Protected Broadcast Driver Architecture (PBDA) service records from a  Program and System Information Protocol (PSIP) table in a Protected Broadcast  Device Architecture (PBDA) transport stream. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDA_Services</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPBDA_Services</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDA_Services</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_services-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694812(v=vs.85)">GetRecordByIndex</a>
</td>
<td align="left" width="63%">
Gets a service record from a specific position in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_services-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a PBDA service record.

</td>
</tr>
</table> 

