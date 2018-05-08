---
UID: NF:taskschd.IMaintenanceSettings.put_Deadline
title: IMaintenanceSettings::put_Deadline
author: windows-driver-content
description: Gets or sets the amount of time after which the Task scheduler attempts to run the task during emergency Automatic maintenance, if the task failed to complete during regular Automatic maintenance.
old-location: taskschd\imaintenancesettings_deadline.htm
old-project: TaskSchd
ms.assetid: 1F0B77C8-82BA-4A7B-A411-CFEFDC9B4CE5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Deadline property [Task Scheduler], Deadline property [Task Scheduler],IMaintenanceSettings interface, IMaintenanceSettings interface [Task Scheduler],Deadline property, IMaintenanceSettings.Deadline, IMaintenanceSettings.put_Deadline, IMaintenanceSettings::Deadline, IMaintenanceSettings::get_Deadline, IMaintenanceSettings::put_Deadline, put_Deadline, taskschd.imaintenancesettings_deadline, taskschd/IMaintenanceSettings::Deadline, taskschd/IMaintenanceSettings::get_Deadline, taskschd/IMaintenanceSettings::put_Deadline
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
-	Taskschd.dll
api_name:
-	IMaintenanceSettings.Deadline
-	IMaintenanceSettings.get_Deadline
-	IMaintenanceSettings.put_Deadline
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMaintenanceSettings::put_Deadline


## -description


Gets or sets the amount of time after which the Task scheduler attempts to run the task during emergency Automatic maintenance, if the task failed to complete during regular Automatic maintenance.

This property is read/write.


## -parameters


## -remarks



The value of this property must be greater than the value of the <a href="https://msdn.microsoft.com/7499C35C-AE46-4F9C-9D81-1FC00B953DFB">Period</a> property.

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/34E33FAE-888E-4E82-83B8-059FB4A64B52">Deadline</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a>
 

 

