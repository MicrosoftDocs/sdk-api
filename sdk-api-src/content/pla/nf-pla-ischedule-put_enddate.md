---
UID: NF:pla.ISchedule.put_EndDate
title: ISchedule::put_EndDate
author: windows-sdk-content
description: Retrieves or sets the last date that the schedule is valid.
old-location: pla\ischedule_enddate.htm
tech.root: pla
ms.assetid: 80a5c1a9-2d0a-4700-824b-1333b5c7c374
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndDate property [PLA], EndDate property [PLA],ISchedule interface, ISchedule interface [PLA],EndDate property, ISchedule.EndDate, ISchedule.put_EndDate, ISchedule::EndDate, ISchedule::get_EndDate, ISchedule::put_EndDate, base.ischedule_enddate, pla.ischedule_enddate, pla/ISchedule::EndDate, pla/ISchedule::get_EndDate, pla/ISchedule::put_EndDate, put_EndDate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - ISchedule.EndDate
 - ISchedule.get_EndDate
 - ISchedule.put_EndDate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISchedule::put_EndDate


## -description


Retrieves or sets the last date that the schedule is valid.

This property is read/write.


## -parameters


## -remarks



The end date must be greater than or equal to the start date.

The set cannot be started after the end date, but if the set is running when the end date is reached, it continues to run.




## -see-also




<a href="https://msdn.microsoft.com/b02043c6-5010-45a1-a4a4-ce30cbf0dba0">ISchedule</a>



<a href="https://msdn.microsoft.com/1bb90c84-0249-4714-9371-d2aed2922d9b">ISchedule::StartDate</a>
 

 

