---
UID: NF:taskschd.ITaskVariables.GetContext
title: ITaskVariables::GetContext (taskschd.h)
description: Used to share the context between different steps and tasks that are in the same job instance.
helpviewer_keywords: ["GetContext","GetContext method [Task Scheduler]","GetContext method [Task Scheduler]","ITaskVariables interface","ITaskVariables interface [Task Scheduler]","GetContext method","ITaskVariables.GetContext","ITaskVariables::GetContext","taskschd.itaskvariables_getcontext","taskschd/ITaskVariables::GetContext"]
old-location: taskschd\itaskvariables_getcontext.htm
tech.root: taskschd
ms.assetid: 090d24ac-18eb-4a76-887f-30d3b99e7ad0
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Task Scheduler], GetContext method [Task Scheduler],ITaskVariables interface, ITaskVariables interface [Task Scheduler],GetContext method, ITaskVariables.GetContext, ITaskVariables::GetContext, taskschd.itaskvariables_getcontext, taskschd/ITaskVariables::GetContext
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
 - ITaskVariables::GetContext
 - taskschd/ITaskVariables::GetContext
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
 - ITaskVariables.GetContext
---

# ITaskVariables::GetContext


## -description

Used to share the context between different steps and tasks that are in the same job instance. This method is not implemented.

## -parameters

### -param pContext [out]

The context that is used to share the context between different steps and tasks that are in the same job instance.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskvariables">ITaskVariables</a>