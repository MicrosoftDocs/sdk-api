---
UID: NN:dvbsiparser.IDVB_EIT
title: IDVB_EIT
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit.htm
old-project: mstv
ms.assetid: 86280e1e-09c3-45a4-bdfb-53eda8e5700e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IDVB_EIT, IDVB_EIT interface [Microsoft TV Technologies], IDVB_EIT interface [Microsoft TV Technologies],described, IDVB_EITInterface, dvbsiparser/IDVB_EIT, mstv.idvb_eit
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
-	IDVB_EIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_EIT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>IDVB_EIT</b> interface enables the client to get information from a DVB event information table (EIT). The <a href="https://msdn.microsoft.com/fd1c0418-2bec-4270-be4b-3877428e3968">IDvbSiParser::GetEIT</a> method returns a pointer to this interface.

An EIT provides information about events in each service, such as the event name, the start time, and the duration. An EIT can hold information about the transport stream that carries it, or it can hold information about other transport streams. There are two types of EITs:
<ul>
<li><i>Present/following</i> EITs contain information about the current event and the next chronological event. This type of EIT can be used to create a simple user interface at the receiver.</li>
<li><i>Schedule</i> EITs contain a list of events that occur after the next event. This type of event can be used to create an electronic program guide (EPG).</li>
</ul>EIT sections are given the following table identifiers (TIDs).
<table>
<tr>
<th>TID</th>
<th>Description</th>
</tr>
<tr>
<td>0x4E</td>
<td>Present/following EIT for this transport stream.</td>
</tr>
<tr>
<td>0x4F</td>
<td>Present/following EIT for another transport stream. </td>
</tr>
<tr>
<td>0x50 – 0x5F</td>
<td>Schedule EIT for this transport stream.</td>
</tr>
<tr>
<td>0x60 – 0x6F</td>
<td>Schedule EIT for another transport stream.</td>
</tr>
</table> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVB_EIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDVB_EIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVB_EIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/634be949-4918-4cae-a282-54cf036d3a09">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea8c91b-f1a2-4c04-933c-c8a2fbfda86f">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b99ab578-fec3-457c-8be2-f0cb65c5b7f7">GetLastTableId</a>
</td>
<td align="left" width="63%">
Returns the last table identifier used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ead94980-0f02-4b21-a569-bcdf0f4b9449">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e477089-faef-4578-ac7f-fea7f1037dfc">GetOriginalNetworkId</a>
</td>
<td align="left" width="63%">
Returns the original network identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85cb6ca7-552d-4d50-ac7f-4a0cb9ec4ad4">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0b8b918-c41c-468c-b289-e3cfc186fa1b">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42a0d194-8c85-41ac-8792-bb8a452d9fab">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the EIT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb480110-0cf4-4b46-af06-f6c42907a184">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Returns the event duration for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfdaea8c-bcc9-4689-94b9-a651fdc06484">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Returns the event identifier for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d154772c-3e7c-49f8-90d1-4ff1be01e4d0">GetRecordFreeCAMode</a>
</td>
<td align="left" width="63%">
Queries whether any of the component streams for an event are scrambled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc5d4bc7-4d56-453f-90ed-6187f55ea464">GetRecordRunningStatus</a>
</td>
<td align="left" width="63%">
Returns the running status of a particular event in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c392620-750d-4219-86fc-4c47109e6a3f">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Returns the event start time for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01edaee4-1968-4e6c-8d4f-e1b518f54aaa">GetSegmentLastSectionNumber</a>
</td>
<td align="left" width="63%">
Returns the section number of the last section in the subtable that contains this section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ff89d80-9c68-4c2a-b0b5-14603b55d7b7">GetServiceId</a>
</td>
<td align="left" width="63%">
Returns the service identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6333813c-e32c-4743-8a7b-98c0a63a66b9">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38b36718-2ec0-4983-8af5-669b05079ff0">GetVersionHash</a>
</td>
<td align="left" width="63%">
Returns a hash value for this table instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3dbd072d-0b48-4ce9-80ec-67f4c3b74915">GetVersionNumber</a>
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
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e54a2bc-c112-4c06-96ff-37de9758df01">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/276c254f-5740-4241-a5ee-82f25885f8c6">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

