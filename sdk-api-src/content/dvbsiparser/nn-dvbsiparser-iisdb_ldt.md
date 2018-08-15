---
UID: NN:dvbsiparser.IISDB_LDT
title: IISDB_LDT
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT). An LDT contains data used to collect reference information from other tables.
old-location: mstv\iisdb_ldt.htm
old-project: mstv
ms.assetid: 4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IISDB_LDT, IISDB_LDT interface [Microsoft TV Technologies], IISDB_LDT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_LDT, mstv.iisdb_ldt
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
 - IISDB_LDT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_LDT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). An LDT contains data used to collect reference
  information from other tables.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an LDT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_LDT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_LDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_LDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da91deea-527c-4458-9db5-ae500cee19bb">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an
  LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a887536d-7ccb-4c28-8ea7-ded90683c036">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/030c01e3-6149-4a61-aeb2-01143642213b">GetOriginalServiceId</a>
</td>
<td align="left" width="63%">
Gets the original_service_id field from
  an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1352eec0-fed2-4d14-81f2-c73b8d34a264">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in
  an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c101068-8a33-4c65-b553-fcd5989c4bd7">GetRecordDescriptionId</a>
</td>
<td align="left" width="63%">
Gets the record description ID from an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a551794a-6051-4c8e-9d44-5938974a6df4">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d1fc08c-9c5b-4361-a144-d8b423250c51">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in
  an LDT for a specific descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/382dc27b-7010-4d05-a401-ded8e0a8c932">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for an LDT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea7f027c-60c3-4dcd-963b-37ae6b088c81">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this instance of an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7567ca34-2898-4066-a81c-348e3ac5c066">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6239688f-2300-4cdb-97cb-179f63efb933">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object by using captured table section data
  for an LDT.

</td>
</tr>
</table> 

