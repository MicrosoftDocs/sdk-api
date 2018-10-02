---
UID: NF:bdatif.IGuideData.GetScheduleEntryProperties
title: IGuideData::GetScheduleEntryProperties
author: windows-sdk-content
description: The GetScheduleEntryProperties method retrieves the properties for a specified schedule entry.
old-location: mstv\iguidedata_getscheduleentryproperties.htm
tech.root: MSTV
ms.assetid: 7fe01a0b-8101-40a2-97ee-e0f5c9d8d1a0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetScheduleEntryProperties, GetScheduleEntryProperties method [Microsoft TV Technologies], GetScheduleEntryProperties method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetScheduleEntryProperties method, IGuideData.GetScheduleEntryProperties, IGuideData::GetScheduleEntryProperties, IGuideDataGetScheduleEntryProperties, bdatif/IGuideData::GetScheduleEntryProperties, mstv.iguidedata_getscheduleentryproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideData.GetScheduleEntryProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideData::GetScheduleEntryProperties


## -description



The <b>GetScheduleEntryProperties</b> method retrieves the properties for a specified schedule entry.




## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier for the schedule entry. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694114(v=VS.85).aspx">IGuideData::GetScheduleEntryIDs</a> method to get a list of schedule entry identifiers.


### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd693993(v=VS.85).aspx">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface


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
<th>Property
            </th>
<th>Description
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
 

The method fails if the TIF has not received the schedule information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/en-us/library/Dd694104(v=VS.85).aspx">IGuideDataEvent::ScheduleEntryChanged</a> event to be fired.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694098(v=VS.85).aspx">IGuideData Interface</a>
 

 

