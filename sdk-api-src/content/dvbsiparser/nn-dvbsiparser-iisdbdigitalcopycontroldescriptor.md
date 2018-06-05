---
UID: NN:dvbsiparser.IIsdbDigitalCopyControlDescriptor
title: IIsdbDigitalCopyControlDescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor.
old-location: mstv\iisdbdigitalcopycontroldescriptor.htm
old-project: mstv
ms.assetid: d509eb58-0c58-4173-8c9c-d52b81932b5c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IIsdbDigitalCopyControlDescriptor, IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies], IIsdbDigitalCopyControlDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbDigitalCopyControlDescriptor, mstv.iisdbdigitalcopycontroldescriptor
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbDigitalCopyControlDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDigitalCopyControlDescriptor interface


## -description


Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) digital copy control descriptor. The digital copy control descriptor appears in the ISDB Service Information as part of the event information table (EIT). Broadcasting service
providers who hold copyrights can use this descriptor to provide data that controls the recording of digital broadcasts and provides copyright data for digital recording equipment. This descriptor also identifies the maximum transmission rate
for each event.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbDigitalCopyControlDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbDigitalCopyControlDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbDigitalCopyControlDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/115ed5f7-a445-4ff2-a9d7-035867b2504d">GetCopyControl</a>
</td>
<td align="left" width="63%">
Gets a code that indicates copy control status from the main body of an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc4e190e-8dd9-4e87-9f85-ed5ecea6eadc">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Gets the number of records in  an ISDB digital copy control descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a0b5433-1681-4b2d-9436-9ed853da6a80">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/800e2263-b04a-4030-9aba-c0b38033b82d">GetRecordCopyControl</a>
</td>
<td align="left" width="63%">
Gets a code that indicates copy control status from a record in an ISDB digital copy control descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e14cb87-3669-4fdf-9c84-b7f2e3c840c2">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB digital copy control descriptor.

</td>
</tr>
</table> 

