---
UID: NN:dvbsiparser.IPBDA_Services
title: IPBDA_Services
author: windows-sdk-content
description: Implements methods that initialize or retrieve Protected Broadcast Driver Architecture (PBDA) service records from a Program and System Information Protocol (PSIP) table in a Protected Broadcast Device Architecture (PBDA) transport stream.
old-location: mstv\ipbda_services.htm
old-project: mstv
ms.assetid: 8d2d62cd-9f62-45d3-8b98-74bb8863c6d6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IPBDA_Services, IPBDA_Services interface [Microsoft TV Technologies], IPBDA_Services interface [Microsoft TV Technologies],described, dvbsiparser/IPBDA_Services, mstv.ipbda_services
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_Services
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDA_Services interface


## -description


Implements methods that initialize or retrieve Protected Broadcast Driver Architecture (PBDA) service records from a  Program and System Information Protocol (PSIP) table in a Protected Broadcast  Device Architecture (PBDA) transport stream. 

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDA_Services</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPBDA_Services</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a39a0ec2-aabc-4609-91cc-667c14773515">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of service records.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f9a71a4-3cfd-4a08-929f-e17d506a021b">GetRecordByIndex</a>
</td>
<td align="left" width="63%">
Gets a service record from a specific position in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2504627a-a5e3-4ed1-9aa2-93d9621bf2e6">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a PBDA service record.

</td>
</tr>
</table> 

