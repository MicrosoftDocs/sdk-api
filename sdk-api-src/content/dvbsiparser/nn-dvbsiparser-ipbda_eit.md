---
UID: NN:dvbsiparser.IPBDA_EIT
title: IPBDA_EIT
author: windows-sdk-content
description: Implements methods that enable the client to get information from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream. The IPBDASiParser::GetEIT method returns a pointer to this interface.
old-location: mstv\ipbda_eit.htm
old-project: mstv
ms.assetid: cb8cd2cc-e498-43c2-ae1e-3543b4ea3b56
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IPBDA_EIT, IPBDA_EIT interface [Microsoft TV Technologies], IPBDA_EIT interface [Microsoft TV Technologies],described, dvbsiparser/IPBDA_EIT, mstv.ipbda_eit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IPBDA_EIT interface


## -description


Implements methods that enable the client to get information from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream. The <a href="https://msdn.microsoft.com/fd1c0418-2bec-4270-be4b-3877428e3968">IPBDASiParser::GetEIT</a> method returns a pointer to this interface.

An EIT provides information about events in each service, such as the event name, the start time, and the duration. An EIT can hold information about the transport stream that carries it, or it can hold information about other transport streams. There are two types of EITs:
<ul>
<li>
          Present/Following EITs contain information about the current event and the next chronological event. This type of EIT can be used to create a simple UI at the receiver.</li>
<li>
          Schedule EITs contain a list of events that occur after the next event. This type of event can be used to create an electronic program guide.</li>
</ul>EIT sections are given the following table identifiers.
<table>
<tr>
<th>Table identifier</th>
<th>Description</th>
</tr>
<tr>
<td>0x80</td>
<td>Present/Following EIT for this transport stream.</td>
</tr>
<tr>
<td>0x81</td>
<td>Schedule EIT for this transport stream. </td>
</tr>
</table> 

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPBDA_EIT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPBDA_EIT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPBDA_EIT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f09421d-ae19-4c8e-93a2-31fa8697742a">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of  event records in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c491b2d0-6426-4a76-b3a1-4477fdf1779c">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Get the number of descriptors associated with an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96ca5a6b-c515-4854-8e95-9cb155879b3b">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Gets an event record descriptor from the EIT based on the record's position in the descriptor list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c711e1-956f-4339-bcaf-78818da540f6">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Gets an event record descriptor from the EIT based on the record's identifying tag.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/898e211c-3228-441d-a099-907676da4bbe">GetRecordDuration</a>
</td>
<td align="left" width="63%">
Gets the event duration from an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c34ad3ee-f4f9-4088-88ae-1340ea503cf5">GetRecordEventId</a>
</td>
<td align="left" width="63%">
Gets the identifier from an  event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7022ac7c-b0ea-4ca1-931f-b09906f67df7">GetRecordStartTime</a>
</td>
<td align="left" width="63%">
Gets the event start time from an event record in the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10e8def6-be78-4b0f-8b47-d0485a1b50f1">GetServiceIdx</a>
</td>
<td align="left" width="63%">
Gets the service identifier from the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4468a632-49e0-4e49-84a4-2ad32c67530b">GetTableId</a>
</td>
<td align="left" width="63%">
Gets the table identifier from the EIT.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16249557-f1e4-4a9f-93bd-b93a2bb72353">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Gets the version number from the EIT.


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

