---
UID: NF:taskschd.IRegisteredTask.GetSecurityDescriptor
title: IRegisteredTask::GetSecurityDescriptor
author: windows-driver-content
description: Gets the security descriptor that is used as credentials for the registered task.
old-location: taskschd\iregisteredtask_getsecuritydescriptor.htm
old-project: TaskSchd
ms.assetid: 474d62a5-9ec7-40f7-b26e-54923f8ebe1e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [Task Scheduler], GetSecurityDescriptor method [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],GetSecurityDescriptor method, IRegisteredTask.GetSecurityDescriptor, IRegisteredTask::GetSecurityDescriptor, taskschd.iregisteredtask_getsecuritydescriptor, taskschd/IRegisteredTask::GetSecurityDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IRegisteredTask.GetSecurityDescriptor
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRegisteredTask::GetSecurityDescriptor


## -description


Gets the security descriptor that is used as credentials for the registered task.


## -parameters




### -param securityInformation

The security information from <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>.


### -param pSddl [out, retval]

The security descriptor that is used as credentials for the registered task.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/9c8ebfdb-3c23-4fec-9023-7a944d99a409">IRegisteredTask::SetSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/9360746e-0f6d-40cb-9135-b12bd8b7d760">ITaskFolder::GetSecurityDescriptor</a>
 

 

