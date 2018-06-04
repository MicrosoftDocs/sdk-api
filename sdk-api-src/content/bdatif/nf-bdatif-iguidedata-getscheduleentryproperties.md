---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IGuideData::GetScheduleEntryProperties


## -description



The <b>GetScheduleEntryProperties</b> method retrieves the properties for a specified schedule entry.




## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier for the schedule entry. Call the <a href="https://msdn.microsoft.com/d44abd0d-bcfc-418f-b541-c085032fb933">IGuideData::GetScheduleEntryIDs</a> method to get a list of schedule entry identifiers.


### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/ae4db426-7e90-4cb6-b53a-2cb7074308fc">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The returned collection includes the following properties.

<table>
<tr>
<th>
              Property
            </th>
<th>
              Description
            </th>
</tr>
<tr>
<td>Description.ID</td>
<td>The unique identifier for the schedule entry.</td>
</tr>
<tr>
<td>Time.Start</td>
<td>The starting time and date of this schedule entry. The value of this property is an unsigned <code>long</code> containing the time and date in GPS time.</td>
</tr>
<tr>
<td>Time.End</td>
<td>The ending time and date of this schedule entry. The value of this property is an unsigned <code>long</code> containing the time and date in GPS time.</td>
</tr>
<tr>
<td>ScheduleEntry.ProgramID</td>
<td>Identifies the program that will play at the time specified by this schedule entry. The value of this property corresponds to the Description.ID property of the program.</td>
</tr>
<tr>
<td>ScheduleEntry.ServiceID</td>
<td>Identifies the service that carries the program represented by this schedule entry. The value of this property corresponds to the Description.ID property of the service.</td>
</tr>
</table>
 

The method fails if the TIF has not received the schedule information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/04c278a0-8a92-4801-9463-696beb22819e">IGuideDataEvent::ScheduleEntryChanged</a> event to be fired.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3bd27fce-90be-480b-b157-a17beccda068">IGuideData Interface</a>
 

 

