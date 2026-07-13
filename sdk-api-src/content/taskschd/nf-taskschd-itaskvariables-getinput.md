---
UID: NF:taskschd.ITaskVariables.GetInput
title: ITaskVariables::GetInput (taskschd.h)
description: Gets the input variables for a task.
helpviewer_keywords: ["GetInput","GetInput method [Task Scheduler]","GetInput method [Task Scheduler]","ITaskVariables interface","ITaskVariables interface [Task Scheduler]","GetInput method","ITaskVariables.GetInput","ITaskVariables::GetInput","taskschd.itaskvariables_getinput","taskschd/ITaskVariables::GetInput"]
old-location: taskschd\itaskvariables_getinput.htm
tech.root: taskschd
ms.assetid: 7c38a633-b3f1-4894-9152-e01a083a54fc
ms.date: 12/05/2018
ms.keywords: GetInput, GetInput method [Task Scheduler], GetInput method [Task Scheduler],ITaskVariables interface, ITaskVariables interface [Task Scheduler],GetInput method, ITaskVariables.GetInput, ITaskVariables::GetInput, taskschd.itaskvariables_getinput, taskschd/ITaskVariables::GetInput
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
 - ITaskVariables::GetInput
 - taskschd/ITaskVariables::GetInput
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
 - ITaskVariables.GetInput
---

# ITaskVariables::GetInput


## -description

Gets the input variables for a task.  This method is not implemented.

## -parameters

### -param pInput [out]

The input variables for a task.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskvariables">ITaskVariables</a>