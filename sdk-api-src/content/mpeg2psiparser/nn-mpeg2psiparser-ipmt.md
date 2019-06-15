---
UID: NN:mpeg2psiparser.IPMT
title: IPMT (mpeg2psiparser.h)
author: windows-sdk-content
description: The IPMT interface enables the client to get information from a program map table (PMT).
old-location: mstv\ipmt.htm
tech.root: mstv
ms.assetid: 0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPMT, IPMT interface [Microsoft TV Technologies], IPMT interface [Microsoft TV Technologies],described, IPMTInterface, mpeg2psiparser/IPMT, mstv.ipmt
ms.topic: interface
req.header: mpeg2psiparser.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPMT interface


## -description



The <b>IPMT</b> interface enables the client to get information from a program map table (PMT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpmt">IAtscPsipParser::GetPMT</a> method returns a pointer to this interface.

The PMT may contain one or more table-wide descriptors. In addition, each record in the PMT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPMT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPMT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPMT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-convertnexttocurrent">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getcountoftabledescriptors">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getnexttable">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getpcrpid">GetPcrPid</a>
</td>
<td align="left" width="63%">
Returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getprogramnumber">GetProgramNumber</a>
</td>
<td align="left" width="63%">
Returns the program number for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecordcountofdescriptors">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecorddescriptorbyindex">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecorddescriptorbytag">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the PMT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecordelementarypid">GetRecordElementaryPid</a>
</td>
<td align="left" width="63%">
Returns the PID for a given elementary stream in the program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getrecordstreamtype">GetRecordStreamType</a>
</td>
<td align="left" width="63%">
Returns the stream type for a given elementary stream in the program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-gettabledescriptorbyindex">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table-wide descriptor for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-gettabledescriptorbytag">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the PMT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-querympeinfo">QueryMPEInfo</a>
</td>
<td align="left" width="63%">
Returns the Multi-Protocol Encapsulation (MPE) information in the PMT, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-queryservicegatewayinfo">QueryServiceGatewayInfo</a>
</td>
<td align="left" width="63%">
Returns the DSM-CC service gateway information in the PMT, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-registerfornexttable">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipmt-registerforwhencurrent">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

