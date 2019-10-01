---
UID: NN:dvbsiparser.IISDB_NBIT
title: IISDB_NBIT (dvbsiparser.h)
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT). The NBIT describes the programs included in a multiplexed transport stream for an ISDB broadcast.
old-location: mstv\iisdb_nbit.htm
tech.root: mstv
ms.assetid: 32c15a03-6683-4b22-b374-a15784696368
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IISDB_NBIT, IISDB_NBIT interface [Microsoft TV Technologies], IISDB_NBIT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_NBIT, mstv.iisdb_nbit
ms.topic: interface
f1_keywords: 
 - "dvbsiparser/IISDB_NBIT"
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
 - IISDB_NBIT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IISDB_NBIT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) network broadcaster information table (NBIT).
  The NBIT describes the programs included in a multiplexed transport stream for an ISDB broadcast.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an NBIT. Then:

<ol>
<li>Query the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_NBIT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_NBIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_NBIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets a value that specifies the number of records in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getoriginalnetworkid">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the network that originated the broadcast.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Gets the number of descriptors from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecorddescriptionbodylocation">GetRecordDescriptionBodyLocation</a>
</td>
<td align="left" width="63%">
Gets a value that indicates where the NBIT contents are described.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd694339(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record
  in an NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets a descriptor from a record in an NBIT
  by using the standard tag for the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordinformationid">GetRecordInformationId</a>
</td>
<td align="left" width="63%">
Gets a value that identifies the type of information in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordinformationtype">GetRecordInformationType</a>
</td>
<td align="left" width="63%">
Gets a value that identifies the type of information obtained from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordkeys">GetRecordKeys</a>
</td>
<td align="left" width="63%">
Gets the key IDs from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordmessagesectionnumber">GetRecordMessageSectionNumber</a>
</td>
<td align="left" width="63%">
Gets a value that identifies a section within the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecordnumberofkeys">GetRecordNumberOfKeys</a>
</td>
<td align="left" width="63%">
Gets the number of key IDs in the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getrecorduserdefined">GetRecordUserDefined</a>
</td>
<td align="left" width="63%">
Gets a broadcaster-defined value from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getversionhash">GetVersionHash</a>
</td>
<td align="left" width="63%">
Gets a hash value for this instance of an NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the NBIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_nbit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that supports this interface.

</td>
</tr>
</table> 

