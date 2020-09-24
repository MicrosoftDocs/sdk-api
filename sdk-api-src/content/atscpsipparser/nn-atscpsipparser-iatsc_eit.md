---
UID: NN:atscpsipparser.IATSC_EIT
title: IATSC_EIT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IATSC_EIT","IATSC_EIT interface [Microsoft TV Technologies]","IATSC_EIT interface [Microsoft TV Technologies]","described","IATSC_EITInterface","atscpsipparser/IATSC_EIT","mstv.iatsc_eit"]
old-location: mstv\iatsc_eit.htm
tech.root: mstv
ms.assetid: ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6
ms.date: 12/05/2018
ms.keywords: IATSC_EIT, IATSC_EIT interface [Microsoft TV Technologies], IATSC_EIT interface [Microsoft TV Technologies],described, IATSC_EITInterface, atscpsipparser/IATSC_EIT, mstv.iatsc_eit
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IATSC_EIT
 - atscpsipparser/IATSC_EIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_EIT
---

# IATSC_EIT interface


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_EIT</b> interface enables the client to get data from an ATSC event information table (EIT). The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteit">IAtscPsipParser::GetEIT</a> method returns a pointer to this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_EIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_EIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_EIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getprotocolversion">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/dd389440(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the EIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordduration">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Returns the event duration for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordetmlocation">GetRecordEtmLocation</a>
</td>
<td align="left" width="63%">
Returns the extended text message (ETM) location for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/mstv/tid">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordstarttime">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Returns the event start time for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecordtitletext">GetRecordTitleText</a>
</td>
<td align="left" width="63%">
Returns the title text for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getsourceid">GetSourceId</a>
</td>
<td align="left" width="63%">
Returns the source identifier for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>