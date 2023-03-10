---
UID: NF:taskschd.ISessionStateChangeTrigger.get_Delay
title: ISessionStateChangeTrigger::get_Delay (taskschd.h)
description: Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected. (ISessionStateChangeTrigger.get_Delay)
helpviewer_keywords: ["Delay property [Task Scheduler]","Delay property [Task Scheduler]","ISessionStateChangeTrigger interface","ISessionStateChangeTrigger interface [Task Scheduler]","Delay property","ISessionStateChangeTrigger.Delay","ISessionStateChangeTrigger.get_Delay","ISessionStateChangeTrigger::Delay","ISessionStateChangeTrigger::get_Delay","ISessionStateChangeTrigger::put_Delay","get_Delay","taskschd.isessionstatechangetrigger_delay","taskschd/ISessionStateChangeTrigger::Delay","taskschd/ISessionStateChangeTrigger::get_Delay","taskschd/ISessionStateChangeTrigger::put_Delay"]
old-location: taskschd\isessionstatechangetrigger_delay.htm
tech.root: taskschd
ms.assetid: 0382b3e7-018d-43e3-893e-b754fe38ed3d
ms.date: 12/05/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler],ISessionStateChangeTrigger interface, ISessionStateChangeTrigger interface [Task Scheduler],Delay property, ISessionStateChangeTrigger.Delay, ISessionStateChangeTrigger.get_Delay, ISessionStateChangeTrigger::Delay, ISessionStateChangeTrigger::get_Delay, ISessionStateChangeTrigger::put_Delay, get_Delay, taskschd.isessionstatechangetrigger_delay, taskschd/ISessionStateChangeTrigger::Delay, taskschd/ISessionStateChangeTrigger::get_Delay, taskschd/ISessionStateChangeTrigger::put_Delay
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISessionStateChangeTrigger::get_Delay
 - taskschd/ISessionStateChangeTrigger::get_Delay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ISessionStateChangeTrigger.Delay
 - ISessionStateChangeTrigger.get_Delay
 - ISessionStateChangeTrigger.put_Delay
---

# ISessionStateChangeTrigger::get_Delay


## -description

Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger">ISessionStateChangeTrigger</a>
