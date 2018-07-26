---
UID: NF:azroles.IAzTask.DeleteTask
title: IAzTask::DeleteTask
author: windows-sdk-content
description: Removes the IAzTask object with the specified name from the task.
old-location: security\iaztask_deletetask.htm
old-project: secauthz
ms.assetid: 1e1288ff-d67b-4180-bfd0-63b81df8f99b
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzTask object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzTask object, DeleteTask method [Security],IAzTask interface, IAzTask interface [Security],DeleteTask method, IAzTask.DeleteTask, IAzTask::DeleteTask, azroles/IAzTask::DeleteTask, security.iaztask_deletetask
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
 - IAzTask.DeleteTask
 - AzTask.DeleteTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::DeleteTask


## -description


The <b>DeleteTask</b> method removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the task.


## -parameters




### -param bstrTask [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to remove from the task.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



