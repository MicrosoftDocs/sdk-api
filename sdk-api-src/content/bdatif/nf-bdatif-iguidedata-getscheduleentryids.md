---
UID: NF:bdatif.IGuideData.GetScheduleEntryIDs
title: IGuideData::GetScheduleEntryIDs (bdatif.h)
description: The GetScheduleEntryIDs method returns a list of unique identifiers for all of the schedule entries contained in all transport streams.
helpviewer_keywords: ["GetScheduleEntryIDs","GetScheduleEntryIDs method [Microsoft TV Technologies]","GetScheduleEntryIDs method [Microsoft TV Technologies]","IGuideData interface","IGuideData interface [Microsoft TV Technologies]","GetScheduleEntryIDs method","IGuideData.GetScheduleEntryIDs","IGuideData::GetScheduleEntryIDs","IGuideDataGetScheduleEntryIDs","bdatif/IGuideData::GetScheduleEntryIDs","mstv.iguidedata_getscheduleentryids"]
old-location: mstv\iguidedata_getscheduleentryids.htm
tech.root: mstv
ms.assetid: d44abd0d-bcfc-418f-b541-c085032fb933
ms.date: 12/05/2018
ms.keywords: GetScheduleEntryIDs, GetScheduleEntryIDs method [Microsoft TV Technologies], GetScheduleEntryIDs method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetScheduleEntryIDs method, IGuideData.GetScheduleEntryIDs, IGuideData::GetScheduleEntryIDs, IGuideDataGetScheduleEntryIDs, bdatif/IGuideData::GetScheduleEntryIDs, mstv.iguidedata_getscheduleentryids
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
 - IGuideData::GetScheduleEntryIDs
 - bdatif/IGuideData::GetScheduleEntryIDs
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
 - IGuideData.GetScheduleEntryIDs
---

# IGuideData::GetScheduleEntryIDs


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetScheduleEntryIDs</b> method returns a list of unique identifiers for all of the schedule entries contained in all transport streams.

## -parameters

### -param pEnumScheduleEntries [out]

Receives a pointer to the <b>IEnumVARIANT</b> interface. Use this interface to enumerate the collection. The caller must release the interface.

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

The method fails if the TIF has not received the schedule information from the PSI tables in the transport stream. The client should implement the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataevent">IGuideDataEvent</a> interface and wait for the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedataevent-scheduleentrychanged">IGuideDataEvent::ScheduleEntryChanged</a> event to be fired.

Each <b>VARIANT</b> type in the collection contains a <b>BSTR</b> that uniquely identifies one schedule entry within the multiplex. To get more information about the schedule entry, pass the <b>VARIANT</b> to the <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getscheduleentryproperties">IGuideData::GetScheduleEntryProperties</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe. Clients should not call methods on the interface from more than one thread.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedata">IGuideData Interface</a>