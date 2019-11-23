---
UID: NN:mpeg2psiparser.IPAT
title: IPAT (mpeg2psiparser.h)

description: The IPAT interface enables the client to get information from a Program Association Table (PAT). The IAtscPsipParser::GetPAT method returns a pointer to this interface.
old-location: mstv\ipat.htm
tech.root: mstv
ms.assetid: 31b0e558-0f22-4761-a964-1908c2835478

ms.date: 12/05/2018
ms.keywords: IPAT, IPAT interface [Microsoft TV Technologies], IPAT interface [Microsoft TV Technologies],described, IPATInterface, mpeg2psiparser/IPAT, mstv.ipat
ms.topic: interface
f1_keywords: 
 - "mpeg2psiparser/IPAT"
dev_langs:
 - c++
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
 - IPAT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPAT interface


## -description



The <b>IPAT</b> interface enables the client to get information from a Program Association Table (PAT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpat">IAtscPsipParser::GetPAT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPAT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPAT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPAT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-convertnexttocurrent">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-findrecordprogrammappid">FindRecordProgramMapPid</a>
</td>
<td align="left" width="63%">
Returns the packet identifier (PID) for the program map table (PMT) associated with a given program number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getcountofrecords">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getnexttable">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getrecordprogrammappid">GetRecordProgramMapPid</a>
</td>
<td align="left" width="63%">
Returns the PID for a given record in the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getrecordprogramnumber">GetRecordProgramNumber</a>
</td>
<td align="left" width="63%">
Retrieves a program number from the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-gettransportstreamid">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-registerfornexttable">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipat-registerforwhencurrent">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

