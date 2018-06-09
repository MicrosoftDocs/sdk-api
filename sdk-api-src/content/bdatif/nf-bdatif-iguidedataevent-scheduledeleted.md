---
UID: NF:bdatif.IGuideDataEvent.ScheduleDeleted
title: IGuideDataEvent::ScheduleDeleted
author: windows-sdk-content
description: The ScheduleDeleted method is called when a schedule entry has been deleted.
old-location: mstv\iguidedataevent_scheduledeleted.htm
old-project: mstv
ms.assetid: 302c068e-4fab-4045-be9b-664902afd44c
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IGuideDataEvent interface [Microsoft TV Technologies],ScheduleDeleted method, IGuideDataEvent.ScheduleDeleted, IGuideDataEvent::ScheduleDeleted, IGuideDataEventScheduleDeleted, ScheduleDeleted, ScheduleDeleted method [Microsoft TV Technologies], ScheduleDeleted method [Microsoft TV Technologies],IGuideDataEvent interface, bdatif/IGuideDataEvent::ScheduleDeleted, mstv.iguidedataevent_scheduledeleted
ms.prod: windows
ms.technology: windows-sdk
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
 - IGuideDataEvent.ScheduleDeleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideDataEvent::ScheduleDeleted


## -description



The <b>ScheduleDeleted</b> method is called when a schedule entry has been deleted.



Currently the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> (TIF) does not support this event, so this method is not called.


## -parameters




### -param varScheduleEntryDescriptionID [in]

Specifies the unique identifier of the schedule entry that was deleted.


## -returns



Return S_OK if successful, or an error code.




## -remarks



The event sink is not required to support this event; it may return E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9da565f2-fbcb-4d71-ae40-7d9821f46630">IGuideDataEvent Interface</a>
 

 

