---
UID: NN:dvbsiparser.IDvbSiParser
title: IDvbSiParser
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IDvbSiParser retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.
old-location: mstv\idvbsiparser.htm
old-project: mstv
ms.assetid: 092162af-5f88-4ce5-ac2f-89327f094804
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDvbSiParser, IDvbSiParser interface [Microsoft TV Technologies], IDvbSiParser interface [Microsoft TV Technologies],described, IDvbSiParserInterface, dvbsiparser/IDvbSiParser, mstv.idvbsiparser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbSiParser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSiParser interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbSiParser</b> retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSiParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbSiParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbSiParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc9cd50f-a9cc-436c-a416-9fc4de506a9e">GetBAT</a>
</td>
<td align="left" width="63%">
Retrieves the bouquet association table (BAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afd6286a-1b05-408f-a752-6fc3a2667e31">GetCAT</a>
</td>
<td align="left" width="63%">
Retrieves the conditional access table (CAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff6d5a04-173d-4577-a6e8-2ae5b2f99358">GetDIT</a>
</td>
<td align="left" width="63%">
Retrieves the discontinuity information table (DIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd1c0418-2bec-4270-be4b-3877428e3968">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7c802ad-908f-4778-b8db-02fff4f3a13e">GetNIT</a>
</td>
<td align="left" width="63%">
Retrieves the network information table (NIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09413d56-e735-4ecf-a505-7d9e2c31d190">GetPAT</a>
</td>
<td align="left" width="63%">
Retrieves the program association table (PAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb8f21f4-fa03-4006-8563-2026e70d5f43">GetPMT</a>
</td>
<td align="left" width="63%">
Retrieves the program map table (PMT) for a specified packet identifier (PID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/263abb39-3f8d-4501-985c-d5ac9b1c9ea1">GetRST</a>
</td>
<td align="left" width="63%">
Retrieves the running status table (RST).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65fe8b2d-31b2-4335-8f5d-9c601e2a64e5">GetSDT</a>
</td>
<td align="left" width="63%">
Retrieves the service description table (SDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d316858e-8014-499c-9727-0a839658fa18">GetSIT</a>
</td>
<td align="left" width="63%">
Retrieves the selection information table (SIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/417f7651-dd6f-4399-8a32-d1b7505efb71">GetST</a>
</td>
<td align="left" width="63%">
Retrieves the stuffing table (ST).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0922ccda-7bd8-480d-8cd1-64f170b7ec69">GetTDT</a>
</td>
<td align="left" width="63%">
Retrieves the time and date table (TDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07e27472-2cb9-4bb1-9976-200bcdccb539">GetTOT</a>
</td>
<td align="left" width="63%">
Retrieves the time offset table (TOT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aae16d0-6852-476b-85a6-6a994400b651">GetTSDT</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream description table (TSDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes this object.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, see the remarks for <a href="https://msdn.microsoft.com/085808e7-b067-470e-9edd-8795f4881485">IDvbSiParser2</a>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

