---
UID: NN:pla.IScheduleCollection
title: IScheduleCollection
author: windows-sdk-content
description: Manages a collection of Schedule objects.To get this interface, access the IDataCollectorSet::Schedules property.
old-location: pla\ischedulecollection.htm
old-project: PLA
ms.assetid: 40b4a77c-5ab4-4443-801c-2e425b6ca1bc
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IScheduleCollection, IScheduleCollection interface [PLA], IScheduleCollection interface [PLA],described, base.ischedulecollection, pla.ischedulecollection, pla/IScheduleCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IScheduleCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
---

# IScheduleCollection interface


## -description


Manages a collection of Schedule objects.

To get this interface, access the <a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">IDataCollectorSet::Schedules</a> property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScheduleCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IScheduleCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IScheduleCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a schedule to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1398bb5-d8a9-49c0-802c-2945428a3e0a">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more schedules to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all schedules from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fa10cd9-d1ae-47c7-80e2-416165164491">CreateSchedule</a>
</td>
<td align="left" width="63%">
Creates a schedule object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a schedule from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScheduleCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of schedules in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested schedule from the collection.

</td>
</tr>
</table> 

