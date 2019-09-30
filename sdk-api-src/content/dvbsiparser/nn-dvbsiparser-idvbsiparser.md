---
UID: NN:dvbsiparser.IDvbSiParser
title: IDvbSiParser (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IDvbSiParser retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.
old-location: mstv\idvbsiparser.htm
tech.root: mstv
ms.assetid: 092162af-5f88-4ce5-ac2f-89327f094804
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbSiParser, IDvbSiParser interface [Microsoft TV Technologies], IDvbSiParser interface [Microsoft TV Technologies],described, IDvbSiParserInterface, dvbsiparser/IDvbSiParser, mstv.idvbsiparser
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDvbSiParser"
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
 - IDvbSiParser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbSiParser interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbSiParser</b> retrieves program specific information (PSI) and service information (SI) tables from a DVB transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbSiParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbSiParser</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getbat">GetBAT</a>
</td>
<td align="left" width="63%">
Retrieves the bouquet association table (BAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getcat">GetCAT</a>
</td>
<td align="left" width="63%">
Retrieves the conditional access table (CAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getdit">GetDIT</a>
</td>
<td align="left" width="63%">
Retrieves the discontinuity information table (DIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">GetEIT</a>
</td>
<td align="left" width="63%">
Retrieves the event information table (EIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">GetNIT</a>
</td>
<td align="left" width="63%">
Retrieves the network information table (NIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getpat">GetPAT</a>
</td>
<td align="left" width="63%">
Retrieves the program association table (PAT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getpmt">GetPMT</a>
</td>
<td align="left" width="63%">
Retrieves the program map table (PMT) for a specified packet identifier (PID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getrst">GetRST</a>
</td>
<td align="left" width="63%">
Retrieves the running status table (RST).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getsdt">GetSDT</a>
</td>
<td align="left" width="63%">
Retrieves the service description table (SDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getsit">GetSIT</a>
</td>
<td align="left" width="63%">
Retrieves the selection information table (SIT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getst">GetST</a>
</td>
<td align="left" width="63%">
Retrieves the stuffing table (ST).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettdt">GetTDT</a>
</td>
<td align="left" width="63%">
Retrieves the time and date table (TDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettot">GetTOT</a>
</td>
<td align="left" width="63%">
Retrieves the time offset table (TOT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettsdt">GetTSDT</a>
</td>
<td align="left" width="63%">
Retrieves the transport stream description table (TSDT).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes this object.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, see the remarks for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser2">IDvbSiParser2</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

