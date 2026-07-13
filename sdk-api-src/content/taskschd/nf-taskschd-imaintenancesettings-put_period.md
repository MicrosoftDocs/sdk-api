---
UID: NF:taskschd.IMaintenanceSettings.put_Period
title: IMaintenanceSettings::put_Period (taskschd.h)
description: Gets or sets the amount of time the task needs to be once executed during regular Automatic maintenance. (Put)
helpviewer_keywords: ["IMaintenanceSettings interface [Task Scheduler]","Period property","IMaintenanceSettings.Period","IMaintenanceSettings.put_Period","IMaintenanceSettings::Period","IMaintenanceSettings::get_Period","IMaintenanceSettings::put_Period","Period property [Task Scheduler]","Period property [Task Scheduler]","IMaintenanceSettings interface","put_Period","taskschd.imaintenancesettings_period","taskschd/IMaintenanceSettings::Period","taskschd/IMaintenanceSettings::get_Period","taskschd/IMaintenanceSettings::put_Period"]
old-location: taskschd\imaintenancesettings_period.htm
tech.root: taskschd
ms.assetid: 7499C35C-AE46-4F9C-9D81-1FC00B953DFB
ms.date: 12/05/2018
ms.keywords: IMaintenanceSettings interface [Task Scheduler],Period property, IMaintenanceSettings.Period, IMaintenanceSettings.put_Period, IMaintenanceSettings::Period, IMaintenanceSettings::get_Period, IMaintenanceSettings::put_Period, Period property [Task Scheduler], Period property [Task Scheduler],IMaintenanceSettings interface, put_Period, taskschd.imaintenancesettings_period, taskschd/IMaintenanceSettings::Period, taskschd/IMaintenanceSettings::get_Period, taskschd/IMaintenanceSettings::put_Period
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
 - IMaintenanceSettings::put_Period
 - taskschd/IMaintenanceSettings::put_Period
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
 - IMaintenanceSettings.Period
 - IMaintenanceSettings.get_Period
 - IMaintenanceSettings.put_Period
---

# IMaintenanceSettings::put_Period


## -description

Gets or sets the amount of time the task needs to be once executed during regular Automatic maintenance.

This property is read/write.

## -parameters

## -remarks

The minimum value for this property is 1 day (<i>P1D</i>).

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-period-element">Period</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-imaintenancesettings">IMaintenanceSettings</a>
