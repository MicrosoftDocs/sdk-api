---
UID: NF:azroles.IAzTask.AddOperation
title: IAzTask::AddOperation (azroles.h)
author: windows-sdk-content
description: Adds the IAzOperation object with the specified name to the task.
old-location: security\iaztask_addoperation.htm
tech.root: SecAuthZ
ms.assetid: 73da7094-440c-4e68-8d43-9f4ba26dd14b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddOperation, AddOperation method [Security], AddOperation method [Security],AzTask object, AddOperation method [Security],IAzTask interface, AzTask object [Security],AddOperation method, IAzTask interface [Security],AddOperation method, IAzTask.AddOperation, IAzTask::AddOperation, azroles/IAzTask::AddOperation, security.iaztask_addoperation
ms.topic: method
f1_keywords: ["azroles/IAzTask.AddOperation"]
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask.AddOperation
 - AzTask.AddOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzTask::AddOperation


## -description


The <b>AddOperation</b> method adds the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name to the task.


## -parameters




### -param bstrOp [in]

Name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to add to the task.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iaztask-submit">Submit</a> method to persist any changes made by this method.



