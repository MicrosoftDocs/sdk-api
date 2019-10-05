---
UID: NN:dvbsiparser.IISDB_BIT
title: IISDB_BIT (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter for each broadcaster unit.
old-location: mstv\iisdb_bit.htm
tech.root: mstv
ms.assetid: 0ec4497c-68c3-4b0e-a9e4-332e42b2c89b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], IISDB_BIT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_BIT, mstv.iisdb_bit
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IISDB_BIT"
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
 - IISDB_BIT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_BIT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter
  for each broadcaster unit.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an BIT. Then:

<ol>
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_BIT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_BIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_BIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getbroadcastviewpropriety">GetBroadcastViewPropriety</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the content is appropriate for an age-based category of viewer from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the number of records in the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of table descriptors in a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordbroadcasterid">GetRecordBroadcasterId</a>
</td>
<td align="left" width="63%">
Gets a BIT record for a specific broadcaster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of descriptors from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694293(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a record in a BIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694295(v=vs.85)">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Gets a descriptor for a specific BIT subtable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a subtable in a BIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of a BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the BIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_bit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that supports this interface.

</td>
</tr>
</table> 

