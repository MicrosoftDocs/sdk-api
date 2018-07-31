---
UID: NF:taskschd.IMaintenanceSettings.put_Period
title: IMaintenanceSettings::put_Period
author: windows-sdk-content
description: Gets or sets the amount of time the task needs to be once executed during regular Automatic maintenance.
old-location: taskschd\imaintenancesettings_period.htm
old-project: TaskSchd
ms.assetid: 7499C35C-AE46-4F9C-9D81-1FC00B953DFB
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMaintenanceSettings interface [Task Scheduler],Period property, IMaintenanceSettings.Period, IMaintenanceSettings.put_Period, IMaintenanceSettings::Period, IMaintenanceSettings::get_Period, IMaintenanceSettings::put_Period, Period property [Task Scheduler], Period property [Task Scheduler],IMaintenanceSettings interface, put_Period, taskschd.imaintenancesettings_period, taskschd/IMaintenanceSettings::Period, taskschd/IMaintenanceSettings::get_Period, taskschd/IMaintenanceSettings::put_Period
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Taskschd.dll
api_name:
 - IMaintenanceSettings.Period
 - IMaintenanceSettings.get_Period
 - IMaintenanceSettings.put_Period
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMaintenanceSettings::put_Period


## -description


Gets or sets the amount of time the task needs to be once executed during regular Automatic maintenance.

This property is read/write.


## -parameters


## -remarks



The minimum value for this property is 1 day (<i>P1D</i>).

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/E4BE2466-3119-41F8-8238-4627C28B26E5">Period</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a>
 

 

