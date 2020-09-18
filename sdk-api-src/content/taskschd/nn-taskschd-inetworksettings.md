---
UID: NN:taskschd.INetworkSettings
title: INetworkSettings (taskschd.h)
description: Provides the settings that the Task Scheduler service uses to obtain a network profile.
helpviewer_keywords: ["INetworkSettings","INetworkSettings interface [Task Scheduler]","INetworkSettings interface [Task Scheduler]","described","taskschd.inetworksettings","taskschd/INetworkSettings"]
old-location: taskschd\inetworksettings.htm
tech.root: taskschd
ms.assetid: 831e1259-df2b-4b03-8336-706727fd7b14
ms.date: 12/05/2018
ms.keywords: INetworkSettings, INetworkSettings interface [Task Scheduler], INetworkSettings interface [Task Scheduler],described, taskschd.inetworksettings, taskschd/INetworkSettings
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
 - INetworkSettings
 - taskschd/INetworkSettings
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
 - INetworkSettings
---

# INetworkSettings interface


## -description

 Provides the settings that the Task Scheduler service uses to obtain a network profile.

## -remarks

When reading or writing your own XML for a task, network settings are specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-networksettings-settingstype-element">NetworkSettings</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>