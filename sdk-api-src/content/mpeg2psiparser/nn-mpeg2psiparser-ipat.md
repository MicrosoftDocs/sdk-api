---
UID: NN:mpeg2psiparser.IPAT
title: IPAT
author: windows-sdk-content
description: The IPAT interface enables the client to get information from a Program Association Table (PAT). The IAtscPsipParser::GetPAT method returns a pointer to this interface.
old-location: mstv\ipat.htm
old-project: mstv
ms.assetid: 31b0e558-0f22-4761-a964-1908c2835478
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IPAT, IPAT interface [Microsoft TV Technologies], IPAT interface [Microsoft TV Technologies],described, IPATInterface, mpeg2psiparser/IPAT, mstv.ipat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT interface


## -description



The <b>IPAT</b> interface enables the client to get information from a Program Association Table (PAT). The <a href="https://msdn.microsoft.com/7cfa9ec0-a802-4dbe-9997-d0eaac2b71c9">IAtscPsipParser::GetPAT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPAT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPAT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/89a493b9-93d3-435f-a4dc-24f8f8e2d1bf">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/148cb123-7cac-46a8-8d60-ce2a28e89230">FindRecordProgramMapPid</a>
</td>
<td align="left" width="63%">
Returns the packet identifier (PID) for the program map table (PMT) associated with a given program number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b73a02e-d6dd-402b-baca-8728cd0fa900">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24cc3c97-60f6-440d-80fd-da7516698a2e">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b1ca2c0-52c4-447a-8191-8f9b69aecd25">GetRecordProgramMapPid</a>
</td>
<td align="left" width="63%">
Returns the PID for a given record in the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24a79c42-aebb-4c31-af86-508c5de3b7a3">GetRecordProgramNumber</a>
</td>
<td align="left" width="63%">
Retrieves a program number from the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a13bb01-47d6-4737-9e66-169def727b5e">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1398a1b9-e9b9-4f30-ba93-0a08a0994cf9">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the PAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/347d8c6f-0934-4ea0-9914-9b4ac47a9306">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a7808b6-2e31-4cd9-a4cc-7a6a7cf46cd4">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

