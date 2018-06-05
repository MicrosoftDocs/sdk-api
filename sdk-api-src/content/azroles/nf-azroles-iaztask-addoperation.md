---
UID: NF:azroles.IAzTask.AddOperation
title: IAzTask::AddOperation
author: windows-sdk-content
description: Adds the IAzOperation object with the specified name to the task.
old-location: security\iaztask_addoperation.htm
old-project: SecAuthZ
ms.assetid: 73da7094-440c-4e68-8d43-9f4ba26dd14b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddOperation, AddOperation method [Security], AddOperation method [Security],AzTask object, AddOperation method [Security],IAzTask interface, AzTask object [Security],AddOperation method, IAzTask interface [Security],AddOperation method, IAzTask.AddOperation, IAzTask::AddOperation, azroles/IAzTask::AddOperation, security.iaztask_addoperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzTask.AddOperation
-	AzTask.AddOperation
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::AddOperation


## -description


The <b>AddOperation</b> method adds the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name to the task.


## -parameters




### -param bstrOp [in]

Name of the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object to add to the task.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a> method to persist any changes made by this method.



