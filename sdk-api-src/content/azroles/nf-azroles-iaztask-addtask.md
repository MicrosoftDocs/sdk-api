---
UID: NF:azroles.IAzTask.AddTask
title: IAzTask::AddTask
author: windows-sdk-content
description: Adds the IAzTask object with the specified name to the task.
old-location: security\iaztask_addtask.htm
old-project: secauthz
ms.assetid: 6b3057d1-26aa-443c-857f-0057ef9d2072
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AddTask, AddTask method [Security], AddTask method [Security],AzTask object, AddTask method [Security],IAzTask interface, AzTask object [Security],AddTask method, IAzTask interface [Security],AddTask method, IAzTask.AddTask, IAzTask::AddTask, azroles/IAzTask::AddTask, security.iaztask_addtask
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask.AddTask
 - AzTask.AddTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::AddTask


## -description


The <b>AddTask</b> method adds the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name to the task.


## -parameters




### -param bstrTask [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to add to the task.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



This method allows the nesting of <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects within another <b>IAzTask</b> object.

You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a> method to persist any changes made by this method.



