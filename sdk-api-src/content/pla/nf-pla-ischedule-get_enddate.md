---
UID: NF:pla.ISchedule.get_EndDate
title: ISchedule::get_EndDate (pla.h)
description: Retrieves or sets the last date that the schedule is valid. (Get)
helpviewer_keywords: ["EndDate property [PLA]","EndDate property [PLA]","ISchedule interface","ISchedule interface [PLA]","EndDate property","ISchedule.EndDate","ISchedule.get_EndDate","ISchedule::EndDate","ISchedule::get_EndDate","ISchedule::put_EndDate","base.ischedule_enddate","get_EndDate","pla.ischedule_enddate","pla/ISchedule::EndDate","pla/ISchedule::get_EndDate","pla/ISchedule::put_EndDate"]
old-location: pla\ischedule_enddate.htm
tech.root: PLA
ms.assetid: 80a5c1a9-2d0a-4700-824b-1333b5c7c374
ms.date: 12/05/2018
ms.keywords: EndDate property [PLA], EndDate property [PLA],ISchedule interface, ISchedule interface [PLA],EndDate property, ISchedule.EndDate, ISchedule.get_EndDate, ISchedule::EndDate, ISchedule::get_EndDate, ISchedule::put_EndDate, base.ischedule_enddate, get_EndDate, pla.ischedule_enddate, pla/ISchedule::EndDate, pla/ISchedule::get_EndDate, pla/ISchedule::put_EndDate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISchedule::get_EndDate
 - pla/ISchedule::get_EndDate
dev_langs:
 - c++
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
---

# ISchedule::get_EndDate


## -description

Retrieves or sets the last date that the schedule is valid.

This property is read/write.

## -parameters

## -remarks

The end date must be greater than or equal to the start date.

The set cannot be started after the end date, but if the set is running when the end date is reached, it continues to run.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ischedule">ISchedule</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ischedule-get_startdate">ISchedule::StartDate</a>
