---
UID: NF:taskschd.IRegisteredTask.SetSecurityDescriptor
title: IRegisteredTask::SetSecurityDescriptor
author: windows-sdk-content
description: Sets the security descriptor that is used as credentials for the registered task.
old-location: taskschd\iregisteredtask_setsecuritydescriptor.htm
tech.root: taskschd
ms.assetid: 9c8ebfdb-3c23-4fec-9023-7a944d99a409
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],SetSecurityDescriptor method, IRegisteredTask.SetSecurityDescriptor, IRegisteredTask::SetSecurityDescriptor, SetSecurityDescriptor, SetSecurityDescriptor method [Task Scheduler], SetSecurityDescriptor method [Task Scheduler],IRegisteredTask interface, taskschd.iregisteredtask_setsecuritydescriptor, taskschd/IRegisteredTask::SetSecurityDescriptor
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRegisteredTask.SetSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegisteredTask::SetSecurityDescriptor


## -description


Sets the security descriptor that is used as credentials for the registered task.


## -parameters




### -param sddl [in]

The security descriptor that is used as credentials for the registered task.

<div class="alert"><b>Note</b>   If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</div>
<div> </div>

### -param flags [in]

Flags that specify how to set the security descriptor. The TASK_DONT_ADD_PRINCIPAL_ACE flag from the <a href="https://msdn.microsoft.com/e8da4d76-25c8-4209-a75b-c77217c366d4">TASK_CREATION</a> enumeration can be specified.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/9c8ebfdb-3c23-4fec-9023-7a944d99a409">IRegisteredTask::SetSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/9360746e-0f6d-40cb-9135-b12bd8b7d760">ITaskFolder::GetSecurityDescriptor</a>
 

 

