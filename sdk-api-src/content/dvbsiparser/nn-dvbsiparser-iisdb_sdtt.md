---
UID: NN:dvbsiparser.IISDB_SDTT
title: IISDB_SDTT (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT). An SDTT contains download information such as service ID, schedule, and receiver types for revision.helpviewer_keywords: ["IISDB_SDTT","IISDB_SDTT interface [Microsoft TV Technologies]","IISDB_SDTT interface [Microsoft TV Technologies]","described","dvbsiparser/IISDB_SDTT","mstv.iisdb_sdtt"]
old-location: mstv\iisdb_sdtt.htm
tech.root: mstv
ms.assetid: f6ed35bc-4470-4000-8f0d-19d454453720
ms.date: 12/05/2018
ms.keywords: IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], IISDB_SDTT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_SDTT, mstv.iisdb_sdtt
f1_keywords:
- dvbsiparser/IISDB_SDTT
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_SDTT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_SDTT</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an
  SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast from an SDTT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordcountofschedules">GetRecordCountOfSchedules</a>
</td>
<td align="left" width="63%">
Returns the number of schedules from a
  record in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694356(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecorddownloadlevel">GetRecordDownloadLevel</a>
</td>
<td align="left" width="63%">
Gets the download level from an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694359(v=vs.85)">GetRecordDurationByIndex</a>
</td>
<td align="left" width="63%">
Receives the event duration from a schedule record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordgroup">GetRecordGroup</a>
</td>
<td align="left" width="63%">
Receives the recording download level from a record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordnewversion">GetRecordNewVersion</a>
</td>
<td align="left" width="63%">
Returns a new version_number field value from a subtable
  record within an
  SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordscheduletimeshiftinformation">GetRecordScheduleTimeShiftInformation</a>
</td>
<td align="left" width="63%">
Receives event time shift information from a schedule record in
    an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694363(v=vs.85)">GetRecordStartTimeByIndex</a>
</td>
<td align="left" width="63%">
Gets an event start time from a schedule record in
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordtargetversion">GetRecordTargetVersion</a>
</td>
<td align="left" width="63%">
Receives the target version from a record 
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getrecordversionindicator">GetRecordVersionIndicator</a>
</td>
<td align="left" width="63%">
Receives the version indicator from a record
  in an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getserviceid">GetServiceId</a>
</td>
<td align="left" width="63%">
Receives the service_id field that uniquely identifies a service from
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-gettableidext">GetTableIdExt</a>
</td>
<td align="left" width="63%">
Gets the table_id_extension field value from
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for
  an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this SDTT instance.
  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number for an SDTT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_sdtt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object by using captured table section data from
  an SDTT.

</td>
</tr>
</table> 

