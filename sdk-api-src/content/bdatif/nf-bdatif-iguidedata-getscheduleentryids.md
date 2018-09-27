---
UID: NF:bdatif.IGuideData.GetScheduleEntryIDs
title: IGuideData::GetScheduleEntryIDs
author: windows-sdk-content
description: The GetScheduleEntryIDs method returns a list of unique identifiers for all of the schedule entries contained in all transport streams.
old-location: mstv\iguidedata_getscheduleentryids.htm
tech.root: MSTV
ms.assetid: d44abd0d-bcfc-418f-b541-c085032fb933
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetScheduleEntryIDs, GetScheduleEntryIDs method [Microsoft TV Technologies], GetScheduleEntryIDs method [Microsoft TV Technologies],IGuideData interface, IGuideData interface [Microsoft TV Technologies],GetScheduleEntryIDs method, IGuideData.GetScheduleEntryIDs, IGuideData::GetScheduleEntryIDs, IGuideDataGetScheduleEntryIDs, bdatif/IGuideData::GetScheduleEntryIDs, mstv.iguidedata_getscheduleentryids
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
 - IGuideData.GetScheduleEntryIDs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideData::GetScheduleEntryIDs


## -description



The <b>GetScheduleEntryIDs</b> method returns a list of unique identifiers for all of the schedule entries contained in all transport streams.




## -parameters




### -param pEnumScheduleEntries

TBD




#### - ppEnumScheduleEntries [out]

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



The method fails if the TIF has not received the schedule information from the PSI tables in the transport stream. The client should implement the <a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent</a> interface and wait for the <a href="https://msdn.microsoft.com/en-us/library/Dd694104(v=VS.85).aspx">IGuideDataEvent::ScheduleEntryChanged</a> event to be fired.

Each <b>VARIANT</b> type in the collection contains a <b>BSTR</b> that uniquely identifies one schedule entry within the multiplex. To get more information about the schedule entry, pass the <b>VARIANT</b> to the <a href="https://msdn.microsoft.com/en-us/library/Dd694115(v=VS.85).aspx">IGuideData::GetScheduleEntryProperties</a> method.

The returned <b>IEnumVARIANT</b> interface is not thread safe. Clients should not call methods on the interface from more than one thread.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694098(v=VS.85).aspx">IGuideData Interface</a>
 

 

