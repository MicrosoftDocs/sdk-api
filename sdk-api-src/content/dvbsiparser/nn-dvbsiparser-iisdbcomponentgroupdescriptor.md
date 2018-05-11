---
UID: NN:dvbsiparser.IIsdbComponentGroupDescriptor
title: IIsdbComponentGroupDescriptor
author: windows-driver-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor.htm
old-project: mstv
ms.assetid: 54ba8ca6-712f-46a1-9ed1-2b20ef8539ba
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IIsdbComponentGroupDescriptor, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies], IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbComponentGroupDescriptor, mstv.iisdbcomponentgroupdescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
-	IIsdbComponentGroupDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbComponentGroupDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) component group descriptor. The component group  descriptor appears in the ISDB service information as part of the event information table (EIT) and describes component grouping in an event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbComponentGroupDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbComponentGroupDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbComponentGroupDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bf17c29-ee43-4de8-a536-bea44238aa53">GetComponentGroupType</a>
</td>
<td align="left" width="63%">
Gets the group type from   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
 Gets the number of component records in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a499d259-460c-428b-ba96-63f71eb556fa">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of  an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97aa98b7-d676-44ad-be93-e58d996a8a6a">GetRecordCAUnitCAUnitId</a>
</td>
<td align="left" width="63%">
Gets the identifier for a conditional access unit in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6588a58-d6df-4f54-ab09-3e938d45f8c4">GetRecordCAUnitComponentTag</a>
</td>
<td align="left" width="63%">
Gets the identifier from a component record that  correspond to a conditional access in   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2656ecfd-84a1-43cb-8fa3-a188f9176c01">GetRecordCAUnitNumberOfComponents</a>
</td>
<td align="left" width="63%">
  Gets the number of records that correspond to a conditional access unit in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/159c496c-675e-458a-b9f9-5c9622fd1848">GetRecordGroupId</a>
</td>
<td align="left" width="63%">
Gets the record group identifier from  an ISDB component group descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/239d952f-908d-4aa9-86c0-f58f7616987f">GetRecordNumberOfCAUnit</a>
</td>
<td align="left" width="63%">
  Gets the number of component records that correspond to a conditional access unit in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0aea8704-cda0-44d5-b06d-79db6ce0114e">GetRecordTextW</a>
</td>
<td align="left" width="63%">
Gets the description of a component group from   an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c84dc9f-933c-4fc8-982c-1f311b94ddf4">GetRecordTotalBitRate</a>
</td>
<td align="left" width="63%">
  Gets the total bit rate from a component record in an ISDB component group descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec33ae30-2e17-4db3-9c08-99447e05686c">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB component group descriptor.

</td>
</tr>
</table> 

