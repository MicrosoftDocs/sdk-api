---
UID: NF:taskschd.IDailyTrigger.get_RandomDelay
title: IDailyTrigger::get_RandomDelay (taskschd.h)
description: Gets or sets a delay time that is randomly added to the start time of the trigger.
helpviewer_keywords: ["IDailyTrigger interface [Task Scheduler]","RandomDelay property","IDailyTrigger.RandomDelay","IDailyTrigger.get_RandomDelay","IDailyTrigger::RandomDelay","IDailyTrigger::get_RandomDelay","IDailyTrigger::put_RandomDelay","RandomDelay property [Task Scheduler]","RandomDelay property [Task Scheduler]","IDailyTrigger interface","get_RandomDelay","taskschd.idailytrigger_randomdelay","taskschd/IDailyTrigger::RandomDelay","taskschd/IDailyTrigger::get_RandomDelay","taskschd/IDailyTrigger::put_RandomDelay"]
old-location: taskschd\idailytrigger_randomdelay.htm
tech.root: taskschd
ms.assetid: d9764132-3329-4d1f-9669-db727c0e904a
ms.date: 12/05/2018
ms.keywords: IDailyTrigger interface [Task Scheduler],RandomDelay property, IDailyTrigger.RandomDelay, IDailyTrigger.get_RandomDelay, IDailyTrigger::RandomDelay, IDailyTrigger::get_RandomDelay, IDailyTrigger::put_RandomDelay, RandomDelay property [Task Scheduler], RandomDelay property [Task Scheduler],IDailyTrigger interface, get_RandomDelay, taskschd.idailytrigger_randomdelay, taskschd/IDailyTrigger::RandomDelay, taskschd/IDailyTrigger::get_RandomDelay, taskschd/IDailyTrigger::put_RandomDelay
f1_keywords:
- taskschd/IDailyTrigger.RandomDelay
dev_langs:
- c++
req.header: taskschd.h
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- IDailyTrigger.RandomDelay
- IDailyTrigger.get_RandomDelay
- IDailyTrigger.put_RandomDelay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDailyTrigger::get_RandomDelay


## -description


Gets or sets a delay time that is randomly added to the start time of the trigger.

This property is read/write.


## -parameters


## -remarks



The specified random delay time is the upper bound for the random interval. The trigger will fire at random during the period specified by the <i>randomDelay</i> parameter, which doesn't begin until the specified start time of the trigger. For example, if the task trigger is set to every seventh day, and the <i>randomDelay</i> parameter is set to P2DT5S (2 day, 5 second time span), then once the seventh day is reached, the trigger will fire once randomly during the next 2 days, 5 seconds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-idailytrigger">IDailyTrigger</a>
 

 

