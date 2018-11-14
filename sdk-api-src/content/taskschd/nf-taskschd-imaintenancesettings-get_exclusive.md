---
UID: NF:taskschd.IMaintenanceSettings.get_Exclusive
title: IMaintenanceSettings::get_Exclusive
author: windows-sdk-content
description: Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.
old-location: taskschd\imaintenancesettings_exclusive.htm
tech.root: TaskSchd
ms.assetid: 6733749B-A82D-4707-93F9-7BD16137C465
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Exclusive property [Task Scheduler], Exclusive property [Task Scheduler],IMaintenanceSettings interface, IMaintenanceSettings interface [Task Scheduler],Exclusive property, IMaintenanceSettings.Exclusive, IMaintenanceSettings.get_Exclusive, IMaintenanceSettings::Exclusive, IMaintenanceSettings::get_Exclusive, IMaintenanceSettings::put_Exclusive, get_Exclusive, taskschd.imaintenancesettings_exclusive, taskschd/IMaintenanceSettings::Exclusive, taskschd/IMaintenanceSettings::get_Exclusive, taskschd/IMaintenanceSettings::put_Exclusive
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Taskschd.dll
api_name:
 - IMaintenanceSettings.Exclusive
 - IMaintenanceSettings.get_Exclusive
 - IMaintenanceSettings.put_Exclusive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- IMaintenanceSettings.get_Exclusive
: 
---

# IMaintenanceSettings::get_Exclusive


## -description


Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode. 


The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task. If exclusivity is not specified, the task is started in parallel with other maintenance tasks.


This property is read/write.


## -parameters


## -remarks



Starting a task in exclusive mode means that no other maintenance task is get started in parallel with this one. Exclusivity does not guarantee the task any priority in order of execution.

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/F690FD8F-BCCB-456D-92E3-25A262D6DCF1">Exclusive</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a>
 

 

