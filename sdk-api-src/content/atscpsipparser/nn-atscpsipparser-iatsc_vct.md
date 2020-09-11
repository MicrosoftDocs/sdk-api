---
UID: NN:atscpsipparser.IATSC_VCT
title: IATSC_VCT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IATSC_VCT","IATSC_VCT interface [Microsoft TV Technologies]","IATSC_VCT interface [Microsoft TV Technologies]","described","IATSC_VCTInterface","atscpsipparser/IATSC_VCT","mstv.iatsc_vct"]
old-location: mstv\iatsc_vct.htm
tech.root: mstv
ms.assetid: 3ff9cd6e-0d25-462c-93a7-2399395f68b0
ms.date: 12/05/2018
ms.keywords: IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], IATSC_VCT interface [Microsoft TV Technologies],described, IATSC_VCTInterface, atscpsipparser/IATSC_VCT, mstv.iatsc_vct
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
 - IATSC_VCT
 - atscpsipparser/IATSC_VCT
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
 - IATSC_VCT
---

# IATSC_VCT interface


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_VCT</b> interface enables the client to get data from a virtual channel table (VCT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getvct">IAtscPsipParser::GetVCT</a> method returns a pointer to this interface.

A <i>record</i> as defined by this interface corresponds to a virtual channel in the VCT. For example, the <b>GetCountOfRecords</b> method returns the number of virtual channels defined in the VCT.

The VCT may contain one or more table-wide descriptors. In addition, each record in the VCT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> method or the <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> method or the <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_VCT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_VCT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_VCT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getprotocolversion">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordcarrierfrequency">GetRecordCarrierFrequency</a>
</td>
<td align="left" width="63%">
Returns the carrier frequency for a channel in this VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd389486(v=vs.85)">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the VCT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordetmlocation">GetRecordEtmLocation</a>
</td>
<td align="left" width="63%">
Returns the extended text message (ETM) location for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordisaccesscontrolledbitset">GetRecordIsAccessControlledBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the access_controlled bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordishiddenbitset">GetRecordIsHiddenBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the hidden bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordishideguidebitset">GetRecordIsHideGuideBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the hide_guide bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordisoutofbandbitset">GetRecordIsOutOfBandBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the out_of_band bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordispathselectbitset">GetRecordIsPathSelectBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the path_select bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordmajorchannelnumber">GetRecordMajorChannelNumber</a>
</td>
<td align="left" width="63%">
Returns the major channel number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordminorchannelnumber">GetRecordMinorChannelNumber</a>
</td>
<td align="left" width="63%">
Returns the minor channel number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordmodulationmode">GetRecordModulationMode</a>
</td>
<td align="left" width="63%">
Returns the modulation mode for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordname">GetRecordName</a>
</td>
<td align="left" width="63%">
Returns the name of a specified channel in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordprogramnumber">GetRecordProgramNumber</a>
</td>
<td align="left" width="63%">
Returns the program number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordservicetype">GetRecordServiceType</a>
</td>
<td align="left" width="63%">
Returns the service type for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordsourceid">GetRecordSourceId</a>
</td>
<td align="left" width="63%">
Returns the source identifier for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getrecordtransportstreamid">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd389502(v=vs.85)">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a table-wide descriptor for the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the VCT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the TSID for the entire VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>

