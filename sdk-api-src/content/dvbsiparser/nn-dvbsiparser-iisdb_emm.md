---
UID: NN:dvbsiparser.IISDB_EMM
title: IISDB_EMM
author: windows-driver-content
description: Gets data from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
old-location: mstv\iisdb_emm.htm
old-project: mstv
ms.assetid: a1389e7c-a3f1-4782-b811-5e09615b3e47
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IISDB_EMM, IISDB_EMM interface [Microsoft TV Technologies], IISDB_EMM interface [Microsoft TV Technologies], described, dvbsiparser/IISDB_EMM, mstv.iisdb_emm
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_EMM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_EMM interface


## -description



  Gets data from an Integrated Services Digital Broadcasting (ISDB)
  entitlement management message (EMM) table. An EMM table contains conditional access data, including contract
  information for subscribers, keys to decrypt common information, and the
  authorization levels or services of specific decoders.



To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an EMM. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_EMM</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_EMM</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/71d92f83-f802-4b5c-a3de-4a2ad675318a">GetDataBytes</a>
</td>
<td align="left" width="63%">
Gets the data contained in the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/311b4efb-dacb-41e1-a798-913e3f99b168">GetIndividualEmmMessage</a>
</td>
<td align="left" width="63%">
Gets an individual EMM message (sent to a specific decoder).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3ad405c-cdf0-4a37-9495-3f126e6c0688">GetSharedEmmMessage</a>
</td>
<td align="left" width="63%">
Gets an shared EMM message (sent to multiple decoders).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa0aba5d-181b-4466-8ad1-5db541d36261">GetTableIdExtension</a>
</td>
<td align="left" width="63%">
Gets the value of the table ID extension field from the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0d97b49-8ab3-4632-9055-e2208b3121e4">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this EMM table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3eebc1cc-044b-4a0a-8259-cb225f829df8">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number for the EMM table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that implements this interface.

</td>
</tr>
</table> 

