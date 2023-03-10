---
UID: NN:taskschd.ITaskVariables
title: ITaskVariables (taskschd.h)
description: Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.
helpviewer_keywords: ["ITaskVariables","ITaskVariables interface [Task Scheduler]","ITaskVariables interface [Task Scheduler]","described","taskschd.itaskvariables","taskschd/ITaskVariables"]
old-location: taskschd\itaskvariables.htm
tech.root: taskschd
ms.assetid: 4f7a9dd3-0bf4-4c23-acdb-a5e0389120cc
ms.date: 12/05/2018
ms.keywords: ITaskVariables, ITaskVariables interface [Task Scheduler], ITaskVariables interface [Task Scheduler],described, taskschd.itaskvariables, taskschd/ITaskVariables
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
 - ITaskVariables
 - taskschd/ITaskVariables
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
 - ITaskVariables
---

# ITaskVariables interface


## -description

Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks. Task handlers that need to input and output data to job variables should do a query interface on the services pointer for <b>ITaskVariables</b>.

## -inheritance

The <b>ITaskVariables</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskVariables</b> also has these types of members:

