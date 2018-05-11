---
UID: NN:dvbsiparser.IDVB_SDT
title: IDVB_SDT
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt.htm
old-project: mstv
ms.assetid: bb473a7e-8957-4e85-98d0-13c6992fbf37
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IDVB_SDT, IDVB_SDT interface [Microsoft TV Technologies], IDVB_SDT interface [Microsoft TV Technologies],described, IDVB_SDTInterface, dvbsiparser/IDVB_SDT, mstv.idvb_sdt
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
-	IDVB_SDT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SDT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_SDT</b> interface enables the client to get information from a service description table (SDT). The <a href="https://msdn.microsoft.com/65fe8b2d-31b2-4335-8f5d-9c601e2a64e5">IDvbSiParser::GetSDT</a> method returns a pointer to this interface.

An SDT describes one or more services that are carried in a particular transport stream. The services may be carried in the same transport stream that carries the SDT, or a different transport stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_SDT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_SDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_SDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05cddb06-1edb-4514-b6fc-21e920e469ea">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9815ba89-d5c2-4d13-8ed1-478953836bc7">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1bc015d-1ea2-4e68-8fbc-39e0bc973d01">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4feebc95-cdcf-443c-bbc1-969575cb795f">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99b7e2ab-c829-4e42-805b-e1ea5b725f82">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acf392b4-519b-4bcc-b0e4-8d5a72442aa5">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4801a47-7cdb-4c31-8bb5-b59df14f0550">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the SDT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93dba50a-c2a5-468d-851a-c43cd986d3ef">GetRecordEITPresentFollowingFlag</a>
</td>
<td align="left" width="63%">
Queries whether the current transport stream contains present/following EIT information for a particular service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f78ebf4-d882-4fdd-90a0-52ad3cd9ca1e">GetRecordEITScheduleFlag</a>
</td>
<td align="left" width="63%">
Queries whether the current transport stream contains schedule EIT information for a particular service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95dfb36b-e6bc-4cfe-bff1-08763a8e245d">GetRecordFreeCAMode</a>
</td>
<td align="left" width="63%">
Queries whether any of the component streams for a particular service are scrambled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6e799b3-f90e-415f-a380-e90d69184fe2">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status of a particular service in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d93d66-f9a6-439c-b0a5-9310d4fa6d88">GetRecordServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier for a record in the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4ecaf56-bc2b-46f3-94e7-aae63ad9be06">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the SDT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56a52beb-d529-4119-a71f-c1f5d671e55b">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea39c890-86d5-4eef-8c50-3edfd0d1ec8d">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the SDT.

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
<a href="https://msdn.microsoft.com/f8040b5a-004a-4428-9906-22aedcd780f6">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/240238fb-54fc-4465-b4dd-4878f43c50a9">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

