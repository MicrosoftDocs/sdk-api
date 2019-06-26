---
UID: NN:dvbsiparser.IISDB_LDT
title: IISDB_LDT (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) linked description table (LDT). An LDT contains data used to collect reference information from other tables.
old-location: mstv\iisdb_ldt.htm
tech.root: mstv
ms.assetid: 4fdf82f2-e931-406b-a8cb-7b24c1d0b8d3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_LDT, IISDB_LDT interface [Microsoft TV Technologies], IISDB_LDT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_LDT, mstv.iisdb_ldt
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IISDB_LDT"
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
 - IISDB_LDT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_LDT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB)
  linked description table (LDT). An LDT contains data used to collect reference
  information from other tables.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an LDT. Then:

<ol>
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_LDT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_LDT</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in an
  LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier that identifies the broadcaster that originated the
  MPEG-2 transport stream from an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getoriginalserviceid">GetOriginalServiceId</a>
</td>
<td align="left" width="63%">
Gets the original_service_id field from
  an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in
  an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getrecorddescriptionid">GetRecordDescriptionId</a>
</td>
<td align="left" width="63%">
Gets the record description ID from an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694327(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in
  an LDT for a specific descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for an LDT. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this instance of an LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the LDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_ldt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object by using captured table section data
  for an LDT.

</td>
</tr>
</table> 

