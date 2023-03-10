---
UID: NF:taskschd.IMaintenanceSettings.get_Deadline
title: IMaintenanceSettings::get_Deadline (taskschd.h)
description: Gets or sets the amount of time after which the Task scheduler attempts to run the task during emergency Automatic maintenance, if the task failed to complete during regular Automatic maintenance. (Get)
helpviewer_keywords: ["Deadline property [Task Scheduler]","Deadline property [Task Scheduler]","IMaintenanceSettings interface","IMaintenanceSettings interface [Task Scheduler]","Deadline property","IMaintenanceSettings.Deadline","IMaintenanceSettings.get_Deadline","IMaintenanceSettings::Deadline","IMaintenanceSettings::get_Deadline","IMaintenanceSettings::put_Deadline","get_Deadline","taskschd.imaintenancesettings_deadline","taskschd/IMaintenanceSettings::Deadline","taskschd/IMaintenanceSettings::get_Deadline","taskschd/IMaintenanceSettings::put_Deadline"]
old-location: taskschd\imaintenancesettings_deadline.htm
tech.root: taskschd
ms.assetid: 1F0B77C8-82BA-4A7B-A411-CFEFDC9B4CE5
ms.date: 12/05/2018
ms.keywords: Deadline property [Task Scheduler], Deadline property [Task Scheduler],IMaintenanceSettings interface, IMaintenanceSettings interface [Task Scheduler],Deadline property, IMaintenanceSettings.Deadline, IMaintenanceSettings.get_Deadline, IMaintenanceSettings::Deadline, IMaintenanceSettings::get_Deadline, IMaintenanceSettings::put_Deadline, get_Deadline, taskschd.imaintenancesettings_deadline, taskschd/IMaintenanceSettings::Deadline, taskschd/IMaintenanceSettings::get_Deadline, taskschd/IMaintenanceSettings::put_Deadline
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMaintenanceSettings::get_Deadline
 - taskschd/IMaintenanceSettings::get_Deadline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Taskschd.dll
api_name:
 - IMaintenanceSettings.Deadline
 - IMaintenanceSettings.get_Deadline
 - IMaintenanceSettings.put_Deadline
---

# IMaintenanceSettings::get_Deadline


## -description

Gets or sets the amount of time after which the Task scheduler attempts to run the task during emergency Automatic maintenance, if the task failed to complete during regular Automatic maintenance.

This property is read/write.

## -parameters

## -remarks

The value of this property must be greater than the value of the <a href="/windows/desktop/api/taskschd/nf-taskschd-imaintenancesettings-get_period">Period</a> property.

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-deadline-element">Deadline</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-imaintenancesettings">IMaintenanceSettings</a>
