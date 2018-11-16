---
UID: NN:dvbsiparser.IISDB_SDTT
title: IISDB_SDTT
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT). An SDTT contains download information such as service ID, schedule, and receiver types for revision.
old-location: mstv\iisdb_sdtt.htm
tech.root: mstv
ms.assetid: f6ed35bc-4470-4000-8f0d-19d454453720
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], IISDB_SDTT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_SDTT, mstv.iisdb_sdtt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IISDB_SDTT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_SDTT interface


## -description


Implements methods that get data
  from an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT). An SDTT contains download information such as service ID, schedule, and
  receiver types for revision.

To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an SDTT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_SDTT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IISDB_SDTT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_SDTT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e445eed-907c-4a9b-80b7-b16460bc131c">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an
  SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49368eaf-3115-4fdf-ac7a-39459d199ce0">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast from an SDTT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04f32111-4c4b-4f5b-81d1-fa7c19841cd8">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8f757de-779c-43df-9f24-caf527e91f03">GetRecordCountOfSchedules</a>
</td>
<td align="left" width="63%">
Returns the number of schedules from a
  record in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8aab681-4858-4ad2-84a7-15a9b8310d6f">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0260e4fb-06d0-489c-8526-f5c2dd62b146">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22903a8d-effc-422b-bca2-907b19703b6d">GetRecordDownloadLevel</a>
</td>
<td align="left" width="63%">
Gets the download level from an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7021a9e-4266-4c17-8874-4b10cf7d6428">GetRecordDurationByIndex</a>
</td>
<td align="left" width="63%">
Receives the event duration from a schedule record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6798e477-754d-49a3-84f1-04d1a60094a7">GetRecordGroup</a>
</td>
<td align="left" width="63%">
Receives the recording download level from a record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a121a8b-10fd-4f78-922a-6be704c2cab4">GetRecordNewVersion</a>
</td>
<td align="left" width="63%">
Returns a new version_number field value from a subtable
  record within an
  SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caf9f0b1-5529-4e8e-ab03-45d7d3268113">GetRecordScheduleTimeShiftInformation</a>
</td>
<td align="left" width="63%">
Receives event time shift information from a schedule record in
    an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccbeb664-6c84-4f50-9376-dfa0492aa9e1">GetRecordStartTimeByIndex</a>
</td>
<td align="left" width="63%">
Gets an event start time from a schedule record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8e85c5b-e577-45b9-b377-c21700c818bb">GetRecordTargetVersion</a>
</td>
<td align="left" width="63%">
Receives the target version from a record 
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b4b4b4b-84b3-4181-bc84-389e72b66053">GetRecordVersionIndicator</a>
</td>
<td align="left" width="63%">
Receives the version indicator from a record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36e9d2b7-f89a-47ad-9fd2-d9aa8d76949c">GetServiceId</a>
</td>
<td align="left" width="63%">
Receives the service_id field that uniquely identifies a service from
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b77ce3b-c706-4820-88dc-08b37978664b">GetTableIdExt</a>
</td>
<td align="left" width="63%">
Gets the table_id_extension field value from
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d73b705f-8409-438e-9f30-3bf2bbf86404">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/269b96c7-7748-44b3-9e6d-2089bcc56664">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this SDTT instance.
  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b2234b-6836-42b7-9e64-a8212946c77b">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number for an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1018e3a-00dd-4964-b491-0193a71e7d51">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object by using captured table section data from
  an SDTT.

</td>
</tr>
</table> 

