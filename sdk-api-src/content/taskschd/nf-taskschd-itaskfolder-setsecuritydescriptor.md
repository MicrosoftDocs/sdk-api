---
UID: NF:taskschd.ITaskFolder.SetSecurityDescriptor
title: ITaskFolder::SetSecurityDescriptor (taskschd.h)
description: Sets the security descriptor for the folder.
helpviewer_keywords: ["ITaskFolder interface [Task Scheduler]","SetSecurityDescriptor method","ITaskFolder.SetSecurityDescriptor","ITaskFolder::SetSecurityDescriptor","SetSecurityDescriptor","SetSecurityDescriptor method [Task Scheduler]","SetSecurityDescriptor method [Task Scheduler]","ITaskFolder interface","taskschd.itaskfolder_setsecuritydescriptor","taskschd/ITaskFolder::SetSecurityDescriptor"]
old-location: taskschd\itaskfolder_setsecuritydescriptor.htm
tech.root: taskschd
ms.assetid: 54f8a37b-87ac-449c-8e03-aeacd27e8c97
ms.date: 12/05/2018
ms.keywords: ITaskFolder interface [Task Scheduler],SetSecurityDescriptor method, ITaskFolder.SetSecurityDescriptor, ITaskFolder::SetSecurityDescriptor, SetSecurityDescriptor, SetSecurityDescriptor method [Task Scheduler], SetSecurityDescriptor method [Task Scheduler],ITaskFolder interface, taskschd.itaskfolder_setsecuritydescriptor, taskschd/ITaskFolder::SetSecurityDescriptor
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
 - ITaskFolder::SetSecurityDescriptor
 - taskschd/ITaskFolder::SetSecurityDescriptor
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
 - ITaskFolder.SetSecurityDescriptor
---

# ITaskFolder::SetSecurityDescriptor


## -description

Sets the security descriptor for the folder.

## -parameters

### -param sddl [in]

The security descriptor for the folder.

<div class="alert"><b>Note</b>   If the Local System account is denied access to a task folder, then the Task Scheduler service can produce unexpected results.</div>
<div> </div>

### -param flags [in]

A value that specifies how the security descriptor is set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.

## -see-also

<a href="/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor">IRegisteredTask::SetSecurityDescriptor</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getsecuritydescriptor">ITaskFolder::GetSecurityDescriptor</a>