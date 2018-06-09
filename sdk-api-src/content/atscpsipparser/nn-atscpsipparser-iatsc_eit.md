---
UID: NN:atscpsipparser.IATSC_EIT
title: IATSC_EIT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit.htm
old-project: mstv
ms.assetid: ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IATSC_EIT, IATSC_EIT interface [Microsoft TV Technologies], IATSC_EIT interface [Microsoft TV Technologies],described, IATSC_EITInterface, atscpsipparser/IATSC_EIT, mstv.iatsc_eit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_EIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_EIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_EIT</b> interface enables the client to get data from an ATSC event information table (EIT). The <a href="https://msdn.microsoft.com/b88a6728-d772-48b8-aebc-7d4cc133320a">IAtscPsipParser::GetEIT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_EIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IATSC_EIT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/edf16862-5bc4-4022-9727-11c1a291417d">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa1234b4-8976-404c-b27d-320d2bba5794">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd568711-c82c-4ffe-9333-2b729502fe79">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06144d3d-b789-4ba3-b313-958de366764f">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdd7f03f-8e03-436f-bfe2-bb46a6a4b415">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the EIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f22a84de-eae3-4981-a38b-6d26fee03c54">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Returns the event duration for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4997f1dc-64b2-4739-90f5-5642a2d71958">GetRecordEtmLocation</a>
</td>
<td align="left" width="63%">
Returns the extended text message (ETM) location for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fb908cf-4ee9-433b-b686-330a32f855af">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c403e86c-0579-47a2-ba87-0d2aec2e186c">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Returns the event start time for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10084fd6-2a14-4abc-8163-ec1b66987343">GetRecordTitleText</a>
</td>
<td align="left" width="63%">
Returns the title text for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab6709e-3d96-4388-a9b2-97a2f04a4eae">GetSourceId</a>
</td>
<td align="left" width="63%">
Returns the source identifier for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/991ec009-4836-4d9a-a7e7-1077464d4964">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the EIT.

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
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

