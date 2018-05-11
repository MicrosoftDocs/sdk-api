---
UID: NN:dvbsiparser.IDVB_SIT
title: IDVB_SIT
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sit.htm
old-project: mstv
ms.assetid: f278d942-a450-4a01-998d-4dac1c8a1fcc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDVB_SIT, IDVB_SIT interface [Microsoft TV Technologies], IDVB_SIT interface [Microsoft TV Technologies],described, IDVB_SITInterface, dvbsiparser/IDVB_SIT, mstv.idvb_sit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dvbsiparser.h
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_SIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_SIT</b> interface enables the client to get information from a selection information table (SIT). The <a href="https://msdn.microsoft.com/d316858e-8014-499c-9727-0a839658fa18">IDvbSiParser::GetSIT</a> method returns a pointer to this interface.

The presence of a SIT in a transport stream indicates that the transport stream is <i>partial</i>, meaning the stream contains a subset of a complete broadcast stream. A partial transport stream does not carry any service information (SI) tables other than SITs and discontinuity information tables (DITs). The SIT contains a summary of the full SI information for the stream.

The SIT may contain one or more table-wide descriptors. In addition, each record in the SIT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_SIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_SIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_SIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1f3fcd9-e386-4a7d-aa46-2c8628d3f71f">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93d04770-9ec5-411c-8892-4b9a7944d681">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fe03fe0-f12e-43cb-b340-26fffdf2d873">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5a23ec2-8eff-42cb-abe2-bf4447406e8c">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b268a08-a09c-4fb0-88ac-25af25654c7a">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6556778-74ea-487c-a6c9-82ed20e79031">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7b05e81-34e5-4a23-8089-9e9d8f2170cc">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the SIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223b7f11-b2fa-4f63-9c9d-bee02e721670">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status of a particular event in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de7c8002-292b-45eb-ba41-1dcd5f55a781">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier for a record in the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e66c7f53-c537-4b56-8cef-2edd43fbedc2">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table-wide descriptor for the SIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85048bfd-1765-44cc-8da5-eeb9698bbfe6">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the SIT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3b40061-8787-42b3-9b2a-39adcb5a3222">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the SIT.

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
<a href="https://msdn.microsoft.com/794c2fb0-ff8d-47b0-9a74-ccdb257a12c7">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a60fa143-0e02-4af8-a64f-1fc92f8e0a3f">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

