---
UID: NF:taskschd.IRegisteredTask.GetSecurityDescriptor
title: IRegisteredTask::GetSecurityDescriptor (taskschd.h)
description: Gets the security descriptor that is used as credentials for the registered task.
helpviewer_keywords: ["GetSecurityDescriptor","GetSecurityDescriptor method [Task Scheduler]","GetSecurityDescriptor method [Task Scheduler]","IRegisteredTask interface","IRegisteredTask interface [Task Scheduler]","GetSecurityDescriptor method","IRegisteredTask.GetSecurityDescriptor","IRegisteredTask::GetSecurityDescriptor","taskschd.iregisteredtask_getsecuritydescriptor","taskschd/IRegisteredTask::GetSecurityDescriptor"]
old-location: taskschd\iregisteredtask_getsecuritydescriptor.htm
tech.root: taskschd
ms.assetid: 474d62a5-9ec7-40f7-b26e-54923f8ebe1e
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [Task Scheduler], GetSecurityDescriptor method [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],GetSecurityDescriptor method, IRegisteredTask.GetSecurityDescriptor, IRegisteredTask::GetSecurityDescriptor, taskschd.iregisteredtask_getsecuritydescriptor, taskschd/IRegisteredTask::GetSecurityDescriptor
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
 - IRegisteredTask::GetSecurityDescriptor
 - taskschd/IRegisteredTask::GetSecurityDescriptor
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
 - IRegisteredTask.GetSecurityDescriptor
---

# IRegisteredTask::GetSecurityDescriptor


## -description

Gets the security descriptor that is used as credentials for the registered task.

## -parameters

### -param securityInformation

The security information from <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>.

### -param pSddl [out, retval]

The security descriptor that is used as credentials for the registered task.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor">IRegisteredTask::SetSecurityDescriptor</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getsecuritydescriptor">ITaskFolder::GetSecurityDescriptor</a>