---
UID: NF:taskschd.ITaskSettings.get_NetworkSettings
title: ITaskSettings::get_NetworkSettings
author: windows-sdk-content
description: Gets or sets the network settings object that contains a network profile identifier and name.
old-location: taskschd\itasksettings_networksettings.htm
old-project: taskschd
ms.assetid: 9ee4f2c0-90bf-4a28-9aeb-0c04f3a197aa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskSettings interface [Task Scheduler],NetworkSettings property, ITaskSettings.NetworkSettings, ITaskSettings.get_NetworkSettings, ITaskSettings::NetworkSettings, ITaskSettings::get_NetworkSettings, ITaskSettings::put_NetworkSettings, NetworkSettings property [Task Scheduler], NetworkSettings property [Task Scheduler],ITaskSettings interface, get_NetworkSettings, taskschd.itasksettings_networksettings, taskschd/ITaskSettings::NetworkSettings, taskschd/ITaskSettings::get_NetworkSettings, taskschd/ITaskSettings::put_NetworkSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.NetworkSettings
 - ITaskSettings.get_NetworkSettings
 - ITaskSettings.put_NetworkSettings
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings::get_NetworkSettings


## -description


Gets or sets the network settings object that contains a network profile identifier and name. If the <a href="https://msdn.microsoft.com/d0926d75-e7d9-469c-aaa0-ddee8fe22dcd">RunOnlyIfNetworkAvailable</a> property of <a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a> is  <b>true</b> and a network propfile is specified in the <b>NetworkSettings</b> property, then the task will run only if the specified network profile is available.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/831e1259-df2b-4b03-8336-706727fd7b14">INetworkSettings</a>



<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>
 

 

