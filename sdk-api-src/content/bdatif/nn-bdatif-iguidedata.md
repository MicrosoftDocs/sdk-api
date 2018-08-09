---
UID: NN:bdatif.IGuideData
title: IGuideData
author: windows-sdk-content
description: The IGuideData interface is exposed by the BDA MPEG-2 Transport Information Filter (TIF). It enables the client to get service information from the MPEG-2 transport stream. Use this interface if you are writing a guide store loader.
old-location: mstv\iguidedata.htm
old-project: mstv
ms.assetid: 3bd27fce-90be-480b-b157-a17beccda068
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGuideData, IGuideData interface [Microsoft TV Technologies], IGuideData interface [Microsoft TV Technologies],described, IGuideDataInterface, bdatif/IGuideData, mstv.iguidedata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdatif.h
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
req.typenames: SmartCardApplication
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IGuideData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideData interface


## -description



The <b>IGuideData</b> interface is exposed by the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> (TIF). It enables the client to get service information from the MPEG-2 transport stream. Use this interface if you are writing a guide store loader.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGuideData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGuideData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGuideData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d182057a-096b-4286-8174-a3ce25c1c86f">GetGuideProgramIDs</a>
</td>
<td align="left" width="63%">
Returns a list of unique identifiers for all of the programs contained in all transport streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57eb55bf-49d9-471e-b59c-0d87aa3c3e3c">GetProgramProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d44abd0d-bcfc-418f-b541-c085032fb933">GetScheduleEntryIDs</a>
</td>
<td align="left" width="63%">
Returns a list of unique identifiers for all of the schedule entries contained in all transport streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fe01a0b-8101-40a2-97ee-e0f5c9d8d1a0">GetScheduleEntryProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified schedule entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28be3bb7-b76a-44a3-892c-2aade5dbe255">GetServiceProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for a specified service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3c08812-ed56-440e-a88d-80e20a681695">GetServices</a>
</td>
<td align="left" width="63%">
Retrieves a collection of tune requests representing all of the services available in the tuning space.

</td>
</tr>
</table> 


## -remarks



The TIF collects service informaton for services, programs, and schedule entries. A service is analogous to a channel; a program is a television show (also known as an "event"); and a schedule entry is an event that occurs at a specific time on a specific service.

For each program and schedule entry, the TIF creates a string that uniquely identifies that element within the multiplex. The <a href="https://msdn.microsoft.com/d182057a-096b-4286-8174-a3ce25c1c86f">GetGuideProgramIDs</a> and <a href="https://msdn.microsoft.com/d44abd0d-bcfc-418f-b541-c085032fb933">GetScheduleEntryIDs</a> methods return a list of these identifiers. You can then pass the identifier to the <a href="https://msdn.microsoft.com/57eb55bf-49d9-471e-b59c-0d87aa3c3e3c">GetProgramProperties</a> and <a href="https://msdn.microsoft.com/7fe01a0b-8101-40a2-97ee-e0f5c9d8d1a0">GetScheduleEntryProperties</a> methods to get additional properties for a particular element.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IGuideData)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

