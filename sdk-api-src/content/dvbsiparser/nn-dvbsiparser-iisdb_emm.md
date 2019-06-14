---
UID: NN:dvbsiparser.IISDB_EMM
title: IISDB_EMM (dvbsiparser.h)
author: windows-sdk-content
description: Gets data from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
old-location: mstv\iisdb_emm.htm
tech.root: mstv
ms.assetid: a1389e7c-a3f1-4782-b811-5e09615b3e47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_EMM, IISDB_EMM interface [Microsoft TV Technologies], IISDB_EMM interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_EMM, mstv.iisdb_emm
ms.topic: interface
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
 - IISDB_EMM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_EMM interface


## -description


Gets data from an Integrated Services Digital Broadcasting (ISDB)
  entitlement management message (EMM) table. An EMM table contains conditional access data, including contract
  information for subscribers, keys to decrypt common information, and the
  authorization levels or services of specific decoders.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an EMM. Then:

<ol>
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_EMM</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_EMM</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_EMM</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-getdatabytes">GetDataBytes</a>
</td>
<td align="left" width="63%">
Gets the data contained in the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-getindividualemmmessage">GetIndividualEmmMessage</a>
</td>
<td align="left" width="63%">
Gets an individual EMM message (sent to a specific decoder).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-getsharedemmmessage">GetSharedEmmMessage</a>
</td>
<td align="left" width="63%">
Gets an shared EMM message (sent to multiple decoders).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-gettableidextension">GetTableIdExtension</a>
</td>
<td align="left" width="63%">
Gets the value of the table ID extension field from the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this EMM table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number for the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_emm-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that implements this interface.

</td>
</tr>
</table> 

