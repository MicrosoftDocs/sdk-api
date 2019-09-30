---
UID: NN:dvbsiparser.IDVB_RST
title: IDVB_RST (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_rst.htm
tech.root: mstv
ms.assetid: deee44cb-92b8-4d10-91d7-c99324ab5832
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDVB_RST, IDVB_RST interface [Microsoft TV Technologies], IDVB_RST interface [Microsoft TV Technologies],described, IDVB_RSTInterface, dvbsiparser/IDVB_RST, mstv.idvb_rst
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IDVB_RST"
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
 - IDVB_RST
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_RST interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_RST</b> interface enables the client to get information from a running status table (RST). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getrst">IDvbSiParser::GetRST</a> method returns a pointer to this interface. The RST enables the provider to update the timing status for one or more events, which may be needed if the schedule changes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_RST</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_RST</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_RST</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordeventid">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordoriginalnetworkid">GetRecordOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordrunningstatus">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordserviceid">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-getrecordtransportstreamid">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a record in the RST.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_rst-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

