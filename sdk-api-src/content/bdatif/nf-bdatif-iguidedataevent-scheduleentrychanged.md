---
UID: NF:bdatif.IGuideDataEvent.ScheduleEntryChanged
title: IGuideDataEvent::ScheduleEntryChanged
author: windows-sdk-content
description: The ScheduleEntryChanged method is called by the TIF when information about one or more schedule entries has changed.
old-location: mstv\iguidedataevent_scheduleentrychanged.htm
old-project: mstv
ms.assetid: 04c278a0-8a92-4801-9463-696beb22819e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ScheduleEntryChanged method, IGuideDataEvent.ScheduleEntryChanged, IGuideDataEvent::ScheduleEntryChanged, IGuideDataEventScheduleEntryChanged, ScheduleEntryChanged, ScheduleEntryChanged method [Microsoft TV Technologies], ScheduleEntryChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ScheduleEntryChanged, mstv.iguidedataevent_scheduleentrychanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.redist: 
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
 - bdatif.h
api_name:
 - IGuideDataEvent.ScheduleEntryChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideDataEvent::ScheduleEntryChanged


## -description



The <b>ScheduleEntryChanged</b> method is called by the TIF when information about one or more schedule entries has changed.




## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier of the program that has changed. Call <a href="https://msdn.microsoft.com/en-us/library/Dd694115(v=VS.85).aspx">IGuideData::GetScheduleEntryProperties</a> to get information about the program. The value of this parameter may be an empty <b>VARIANT</b> type (VT_EMPTY); if so, examine all of the programs to determine which ones have changed.


## -returns



Return S_OK if successful, or an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent Interface</a>
 

 

