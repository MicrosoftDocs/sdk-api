---
UID: NN:dvbsiparser.IIsdbSiParser2
title: IIsdbSiParser2 (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that retrieve program specific information (PSI) tables and service information tables from an Integrated Services Digital Broadcast (ISDB) transport stream.
old-location: mstv\iisdbsiparser2.htm
tech.root: mstv
ms.assetid: d8dfc713-aaa4-46b1-8eca-2e132a9d705f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IIsdbSiParser2, IIsdbSiParser2 interface [Microsoft TV Technologies], IIsdbSiParser2 interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbSiParser2, mstv.iisdbsiparser2
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbSiParser2"
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
 - IIsdbSiParser2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbSiParser2 interface


## -description


Implements methods that retrieve program specific information (PSI) tables and service information tables from an Integrated Services Digital Broadcast (ISDB) transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbSiParser2</b> interface inherits from <b>IDvbSiParser2</b>. <b>IIsdbSiParser2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbSiParser2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getbit">GetBIT</a>
</td>
<td align="left" width="63%">
 Retrieves the broadcaster information table (BIT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getcdt">GetCDT</a>
</td>
<td align="left" width="63%">
Retrieves the common data table (CDT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getemm">GetEMM</a>
</td>
<td align="left" width="63%">
Retrieves the entitlement management message (EMM) table  from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getldt">GetLDT</a>
</td>
<td align="left" width="63%">
Retrieves the linked description table (LDT)
  from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getnbit">GetNBIT</a>
</td>
<td align="left" width="63%">
 Retrieves the
   network broadcaster information table (NBIT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getsdt">GetSDT</a>
</td>
<td align="left" width="63%">
Retrieves the service description table (SDT) from an ISDB transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparser2-getsdtt">GetSDTT</a>
</td>
<td align="left" width="63%">
Retrieves the  software download
  trigger table
  (SDTT)  from an ISDB transport stream.

</td>
</tr>
</table> 

