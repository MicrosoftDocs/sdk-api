---
UID: NF:taskschd.ITaskSettings.put_NetworkSettings
title: ITaskSettings::put_NetworkSettings (taskschd.h)
description: Gets or sets the network settings object that contains a network profile identifier and name. (Put)
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","NetworkSettings property","ITaskSettings.NetworkSettings","ITaskSettings.put_NetworkSettings","ITaskSettings::NetworkSettings","ITaskSettings::get_NetworkSettings","ITaskSettings::put_NetworkSettings","NetworkSettings property [Task Scheduler]","NetworkSettings property [Task Scheduler]","ITaskSettings interface","put_NetworkSettings","taskschd.itasksettings_networksettings","taskschd/ITaskSettings::NetworkSettings","taskschd/ITaskSettings::get_NetworkSettings","taskschd/ITaskSettings::put_NetworkSettings"]
old-location: taskschd\itasksettings_networksettings.htm
tech.root: taskschd
ms.assetid: 9ee4f2c0-90bf-4a28-9aeb-0c04f3a197aa
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],NetworkSettings property, ITaskSettings.NetworkSettings, ITaskSettings.put_NetworkSettings, ITaskSettings::NetworkSettings, ITaskSettings::get_NetworkSettings, ITaskSettings::put_NetworkSettings, NetworkSettings property [Task Scheduler], NetworkSettings property [Task Scheduler],ITaskSettings interface, put_NetworkSettings, taskschd.itasksettings_networksettings, taskschd/ITaskSettings::NetworkSettings, taskschd/ITaskSettings::get_NetworkSettings, taskschd/ITaskSettings::put_NetworkSettings
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
 - ITaskSettings::put_NetworkSettings
 - taskschd/ITaskSettings::put_NetworkSettings
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
 - ITaskSettings.NetworkSettings
 - ITaskSettings.get_NetworkSettings
 - ITaskSettings.put_NetworkSettings
---

# ITaskSettings::put_NetworkSettings


## -description

Gets or sets the network settings object that contains a network profile identifier and name. If the <a href="/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable">RunOnlyIfNetworkAvailable</a> property of <a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a> is  <b>true</b> and a network propfile is specified in the <b>NetworkSettings</b> property, then the task will run only if the specified network profile is available.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-inetworksettings">INetworkSettings</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>
