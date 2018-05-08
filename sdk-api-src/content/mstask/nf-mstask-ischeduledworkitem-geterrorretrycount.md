---
UID: NF:mstask.IScheduledWorkItem.GetErrorRetryCount
title: IScheduledWorkItem::GetErrorRetryCount
author: windows-driver-content
description: Retrieves the number of times that the Task Scheduler will retry an operation when an error occurs. This method is not implemented.
old-location: taskschd\ischeduledworkitem_geterrorretrycount.htm
old-project: TaskSchd
ms.assetid: f9935325-124b-4c21-be9c-e9d48fb69791
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetErrorRetryCount, GetErrorRetryCount method [Task Scheduler], GetErrorRetryCount method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetErrorRetryCount method, IScheduledWorkItem.GetErrorRetryCount, IScheduledWorkItem::GetErrorRetryCount, _msb_ischeduledworkitem_geterrorretrycount, mstask/IScheduledWorkItem::GetErrorRetryCount, taskschd.ischeduledworkitem_geterrorretrycount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.GetErrorRetryCount
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IScheduledWorkItem::GetErrorRetryCount


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the number of times that the Task Scheduler will retry an operation when an error occurs. This method is not implemented.


## -parameters




### -param pwRetryCount [out]

A pointer to a <b>WORD</b> that contains the number of times to retry.


## -returns



Not implemented.




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/f2c5bafb-a792-4653-87ab-677daec9b10f">SetErrorRetryCount</a>
 

 

