---
UID: NS:mstask._DAILY
title: "_DAILY"
author: windows-driver-content
description: Defines the interval, in days, at which a task is run.
old-location: taskschd\daily.htm
old-project: TaskSchd
ms.assetid: 4dbab308-fd1c-4be4-84f6-c12f751ab29e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: DAILY, DAILY structure [Task Scheduler], _DAILY, _msb_daily, mstask/DAILY, taskschd.daily, triggers [Task Scheduler], structures, DAILY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DAILY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mstask.h
api_name:
-	DAILY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _DAILY structure


## -description


 Defines the interval, in days, at which a task is run.


## -struct-fields




### -field DaysInterval

Specifies the number of days between task runs.


## -remarks



 The 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure definition.




## -see-also




<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a>
 

 

