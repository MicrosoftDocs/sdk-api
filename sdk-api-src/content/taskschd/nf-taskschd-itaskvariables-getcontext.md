---
UID: NF:taskschd.ITaskVariables.GetContext
title: ITaskVariables::GetContext
author: windows-sdk-content
description: Used to share the context between different steps and tasks that are in the same job instance.
old-location: taskschd\itaskvariables_getcontext.htm
old-project: taskschd
ms.assetid: 090d24ac-18eb-4a76-887f-30d3b99e7ad0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetContext, GetContext method [Task Scheduler], GetContext method [Task Scheduler],ITaskVariables interface, ITaskVariables interface [Task Scheduler],GetContext method, ITaskVariables.GetContext, ITaskVariables::GetContext, taskschd.itaskvariables_getcontext, taskschd/ITaskVariables::GetContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITaskVariables.GetContext
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskVariables::GetContext


## -description


Used to share the context between different steps and tasks that are in the same job instance. This method is not implemented.


## -parameters




### -param pContext [out]

The context that is used to share the context between different steps and tasks that are in the same job instance.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4f7a9dd3-0bf4-4c23-acdb-a5e0389120cc">ITaskVariables</a>
 

 

