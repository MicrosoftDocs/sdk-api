---
UID: NF:taskschd.ITaskFolder.GetSecurityDescriptor
title: ITaskFolder::GetSecurityDescriptor (taskschd.h)

description: Gets the security descriptor for the folder.
old-location: taskschd\itaskfolder_getsecuritydescriptor.htm
tech.root: taskschd
ms.assetid: 9360746e-0f6d-40cb-9135-b12bd8b7d760

ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [Task Scheduler], GetSecurityDescriptor method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetSecurityDescriptor method, ITaskFolder.GetSecurityDescriptor, ITaskFolder::GetSecurityDescriptor, taskschd.itaskfolder_getsecuritydescriptor, taskschd/ITaskFolder::GetSecurityDescriptor
ms.topic: method
f1_keywords: 
 - "taskschd/ITaskFolder.GetSecurityDescriptor"
dev_langs:
 - c++
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
 - ITaskFolder.GetSecurityDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskFolder::GetSecurityDescriptor


## -description


Gets the security descriptor for the folder.


## -parameters




### -param securityInformation [in]

The security information from <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a>.


### -param pSddl [out]

The security descriptor for the folder.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor">IRegisteredTask::SetSecurityDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor">ITaskFolder::SetSecurityDescriptor</a>
 

 

