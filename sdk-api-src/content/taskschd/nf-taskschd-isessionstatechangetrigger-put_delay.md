---
UID: NF:taskschd.ISessionStateChangeTrigger.put_Delay
title: ISessionStateChangeTrigger::put_Delay method
author: windows-driver-content
description: Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.
old-location: taskschd\isessionstatechangetrigger_delay.htm
old-project: TaskSchd
ms.assetid: 0382b3e7-018d-43e3-893e-b754fe38ed3d
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Delay property [Task Scheduler], Delay property [Task Scheduler], ISessionStateChangeTrigger interface, ISessionStateChangeTrigger, ISessionStateChangeTrigger interface [Task Scheduler], Delay property, ISessionStateChangeTrigger.Delay, ISessionStateChangeTrigger::get_Delay, ISessionStateChangeTrigger::put_Delay, put_Delay,ISessionStateChangeTrigger.put_Delay, taskschd.isessionstatechangetrigger_delay, taskschd/ISessionStateChangeTrigger::Delay, taskschd/ISessionStateChangeTrigger::get_Delay, taskschd/ISessionStateChangeTrigger::put_Delay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ISessionStateChangeTrigger.Delay
-	ISessionStateChangeTrigger.get_Delay
-	ISessionStateChangeTrigger.put_Delay
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISessionStateChangeTrigger::put_Delay method


## -description


Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected. The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/0bf56d67-6c44-4978-93a9-7b525f2bf140">ISessionStateChangeTrigger</a>
 

 

