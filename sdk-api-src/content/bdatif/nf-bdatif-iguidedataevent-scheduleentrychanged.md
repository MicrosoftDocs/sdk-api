---
UID: NF:bdatif.IGuideDataEvent.ScheduleEntryChanged
title: IGuideDataEvent::ScheduleEntryChanged
author: windows-sdk-content
description: The ScheduleEntryChanged method is called by the TIF when information about one or more schedule entries has changed.
old-location: mstv\iguidedataevent_scheduleentrychanged.htm
tech.root: mstv
ms.assetid: 04c278a0-8a92-4801-9463-696beb22819e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ScheduleEntryChanged method, IGuideDataEvent.ScheduleEntryChanged, IGuideDataEvent::ScheduleEntryChanged, IGuideDataEventScheduleEntryChanged, ScheduleEntryChanged, ScheduleEntryChanged method [Microsoft TV Technologies], ScheduleEntryChanged method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ScheduleEntryChanged, mstv.iguidedataevent_scheduleentrychanged
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
 - IGuideDataEvent.ScheduleEntryChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent::ScheduleEntryChanged


## -description



The <b>ScheduleEntryChanged</b> method is called by the TIF when information about one or more schedule entries has changed.




## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier of the program that has changed. Call <a href="https://msdn.microsoft.com/7fe01a0b-8101-40a2-97ee-e0f5c9d8d1a0">IGuideData::GetScheduleEntryProperties</a> to get information about the program. The value of this parameter may be an empty <b>VARIANT</b> type (VT_EMPTY); if so, examine all of the programs to determine which ones have changed.


## -returns



Return S_OK if successful, or an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent Interface</a>
 

 

