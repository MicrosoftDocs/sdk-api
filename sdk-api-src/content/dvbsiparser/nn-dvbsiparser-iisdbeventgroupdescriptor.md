---
UID: NN:dvbsiparser.IIsdbEventGroupDescriptor
title: IIsdbEventGroupDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
old-location: mstv\iisdbeventgroupdescriptor.htm
old-project: mstv
ms.assetid: 1e71f277-0296-4589-8099-dfae2a9dcfb0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IIsdbEventGroupDescriptor, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies], IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbEventGroupDescriptor, mstv.iisdbeventgroupdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbEventGroupDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbEventGroupDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) event group descriptor. The event group  descriptor appears in the ISDB service information as part of the event information table (EIT) and describes a group of related events. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbEventGroupDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbEventGroupDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbEventGroupDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a254840c-c6bd-4245-a0fc-b0b0b63e637a">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of event records in   an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdc3c99d-516d-4001-a261-2d909b17a1f1">GetCountOfRefRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of records for related events from an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/152bae4a-f4e6-4e9e-a1ed-19240cf8108c">GetGroupType</a>
</td>
<td align="left" width="63%">
 Gets a code that describes the group type from an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08e61ddb-15d5-40e3-9e37-7c45d1f18b4a">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/899c8c7f-9e85-4b0d-b7ea-24fb0b5daa88">GetRecordEvent</a>
</td>
<td align="left" width="63%">
 Gets data from an event record in an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fede6a0e-5ac1-472e-aaa8-9d31737a8a1d">GetRefRecordEvent</a>
</td>
<td align="left" width="63%">
 Gets data from a related event record in an ISDB event group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/249c57a6-dcf8-4701-975d-39f8e8735798">GetTag</a>
</td>
<td align="left" width="63%">
 Gets the tag that identifies an ISDB event group descriptor.

</td>
</tr>
</table> 

