---
UID: NF:taskschd.ITaskFolder.SetSecurityDescriptor
title: ITaskFolder::SetSecurityDescriptor
author: windows-sdk-content
description: Sets the security descriptor for the folder.
old-location: taskschd\itaskfolder_setsecuritydescriptor.htm
tech.root: TaskSchd
ms.assetid: 54f8a37b-87ac-449c-8e03-aeacd27e8c97
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITaskFolder interface [Task Scheduler],SetSecurityDescriptor method, ITaskFolder.SetSecurityDescriptor, ITaskFolder::SetSecurityDescriptor, SetSecurityDescriptor, SetSecurityDescriptor method [Task Scheduler], SetSecurityDescriptor method [Task Scheduler],ITaskFolder interface, taskschd.itaskfolder_setsecuritydescriptor, taskschd/ITaskFolder::SetSecurityDescriptor
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
 - ITaskFolder.SetSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- ITaskFolder.SetSecurityDescriptor
: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.




## -see-also




<a href="https://msdn.microsoft.com/9c8ebfdb-3c23-4fec-9023-7a944d99a409">IRegisteredTask::SetSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/9360746e-0f6d-40cb-9135-b12bd8b7d760">ITaskFolder::GetSecurityDescriptor</a>
 

 

