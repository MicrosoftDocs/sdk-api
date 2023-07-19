---
UID: NF:bdatif.IGuideData.GetScheduleEntryProperties
title: IGuideData::GetScheduleEntryProperties (bdatif.h)
description: The GetScheduleEntryProperties method retrieves the properties for a specified schedule entry.
helpviewer_keywords: ["GetScheduleEntryProperties","GetScheduleEntryProperties method [Microsoft TV Technologies]","GetScheduleEntryProperties method [Microsoft TV Technologies]","IGuideData interface","IGuideData interface [Microsoft TV Technologies]","GetScheduleEntryProperties method","IGuideData.GetScheduleEntryProperties","IGuideData::GetScheduleEntryProperties","IGuideDataGetScheduleEntryProperties","bdatif/IGuideData::GetScheduleEntryProperties","mstv.iguidedata_getscheduleentryproperties"]
old-location: mstv\iguidedata_getscheduleentryproperties.htm
tech.root: mstv
ms.assetid: 7fe01a0b-8101-40a2-97ee-e0f5c9d8d1a0
ms.date: 12/05/2018
ms.keywords: GetScheduleEntryProperties, GetScheduleEntryProperties method [Microsoft TV Technologies], GetScheduleEntryProperties method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetScheduleEntryProperties method, IGuideData.GetScheduleEntryProperties, IGuideData::GetScheduleEntryProperties, IGuideDataGetScheduleEntryProperties, bdatif/IGuideData::GetScheduleEntryProperties, mstv.iguidedata_getscheduleentryproperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideData::GetScheduleEntryProperties
 - bdatif/IGuideData::GetScheduleEntryProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideData.GetScheduleEntryProperties
---

# IGuideData::GetScheduleEntryProperties


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetScheduleEntryProperties</b> method retrieves the properties for a specified schedule entry.

## -parameters

### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier for the schedule entry. Call the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryids">IGuideData::GetScheduleEntryIDs</a> method to get a list of schedule entry identifiers.

### -param ppEnumProperties [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumguidedataproperties">IEnumGuideDataProperties</a> interface pointer. Use this interface to enumerate the properties. The caller must release the interface

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
 

The method fails if the TIF has not received the schedule information from the PSI tables in the transport stream. The client should implement the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent</a> interface and wait for the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-scheduleentrychanged">IGuideDataEvent::ScheduleEntryChanged</a> event to be fired.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedata">IGuideData Interface</a>