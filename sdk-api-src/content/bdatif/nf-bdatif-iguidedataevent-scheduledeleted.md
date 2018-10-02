---
UID: NF:bdatif.IGuideDataEvent.ScheduleDeleted
title: IGuideDataEvent::ScheduleDeleted
author: windows-sdk-content
description: The ScheduleDeleted method is called when a schedule entry has been deleted.
old-location: mstv\iguidedataevent_scheduledeleted.htm
tech.root: MSTV
ms.assetid: 302c068e-4fab-4045-be9b-664902afd44c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ScheduleDeleted method, IGuideDataEvent.ScheduleDeleted, IGuideDataEvent::ScheduleDeleted, IGuideDataEventScheduleDeleted, ScheduleDeleted, ScheduleDeleted method [Microsoft TV Technologies], ScheduleDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ScheduleDeleted, mstv.iguidedataevent_scheduledeleted
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
 - IGuideDataEvent.ScheduleDeleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataEvent::ScheduleDeleted


## -description



The <b>ScheduleDeleted</b> method is called when a schedule entry has been deleted.



Currently the <a href="https://msdn.microsoft.com/en-us/library/Dd693011(v=VS.85).aspx">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.


## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier of the schedule entry that was deleted.


## -returns



Return S_OK if successful, or an error code.




## -remarks



The event sink is not required to support this event; it may return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694099(v=VS.85).aspx">IGuideDataEvent Interface</a>
 

 

