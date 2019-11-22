---
UID: NN:dvbsiparser.IIsdbCADescriptor
title: IIsdbCADescriptor (dvbsiparser.h)

description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) descriptor.
old-location: mstv\iisdbcadescriptor.htm
tech.root: mstv
ms.assetid: 6683f3db-636b-42bb-a46d-c175a4324023

ms.date: 12/05/2018
ms.keywords: IIsdbCADescriptor, IIsdbCADescriptor interface [Microsoft TV Technologies], IIsdbCADescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCADescriptor, mstv.iisdbcadescriptor
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IIsdbCADescriptor"
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
 - IIsdbCADescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCADescriptor interface


## -description


 Implements methods that get data from  an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) descriptor. The CA descriptor appears in the ISDB service information as part of the conditional access table (CAT) or program map table (PMT) and indicates the program identifiers (PIDs) of transport stream packets that contain entitlement control message (ECM) data or entitlement management message (EMM) data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCADescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbCADescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbCADescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-getcapid">GetCAPID</a>
</td>
<td align="left" width="63%">
Gets the CA  program identifier (PID) from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-getcasystemid">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the conditional-access system identifier from an ISDB CA descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB conditional access descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-getprivatedatabytes">GetPrivateDataBytes</a>
</td>
<td align="left" width="63%">
Gets private data bytes from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-getreservedbits">GetReservedBits</a>
</td>
<td align="left" width="63%">
Gets the reserved bits from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcadescriptor-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB CA descriptor.

</td>
</tr>
</table> 

