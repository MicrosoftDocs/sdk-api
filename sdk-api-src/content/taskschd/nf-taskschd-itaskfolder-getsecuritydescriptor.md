---
UID: NF:taskschd.ITaskFolder.GetSecurityDescriptor
title: ITaskFolder::GetSecurityDescriptor (taskschd.h)
description: Gets the security descriptor for the folder.
helpviewer_keywords: ["GetSecurityDescriptor","GetSecurityDescriptor method [Task Scheduler]","GetSecurityDescriptor method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","GetSecurityDescriptor method","ITaskFolder.GetSecurityDescriptor","ITaskFolder::GetSecurityDescriptor","taskschd.itaskfolder_getsecuritydescriptor","taskschd/ITaskFolder::GetSecurityDescriptor"]
old-location: taskschd\itaskfolder_getsecuritydescriptor.htm
tech.root: taskschd
ms.assetid: 9360746e-0f6d-40cb-9135-b12bd8b7d760
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [Task Scheduler], GetSecurityDescriptor method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetSecurityDescriptor method, ITaskFolder.GetSecurityDescriptor, ITaskFolder::GetSecurityDescriptor, taskschd.itaskfolder_getsecuritydescriptor, taskschd/ITaskFolder::GetSecurityDescriptor
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
 - ITaskFolder::GetSecurityDescriptor
 - taskschd/ITaskFolder::GetSecurityDescriptor
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
 - ITaskFolder.GetSecurityDescriptor
---

# ITaskFolder::GetSecurityDescriptor


## -description

Gets the security descriptor for the folder.

## -parameters

### -param securityInformation [in]

The security information from <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>.

### -param pSddl [out]

The security descriptor for the folder.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor">IRegisteredTask::SetSecurityDescriptor</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor">ITaskFolder::SetSecurityDescriptor</a>