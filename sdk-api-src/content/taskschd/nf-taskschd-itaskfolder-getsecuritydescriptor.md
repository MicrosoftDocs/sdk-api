---
UID: NF:taskschd.ITaskFolder.GetSecurityDescriptor
title: ITaskFolder::GetSecurityDescriptor
author: windows-sdk-content
description: Gets the security descriptor for the folder.
old-location: taskschd\itaskfolder_getsecuritydescriptor.htm
old-project: TaskSchd
ms.assetid: 9360746e-0f6d-40cb-9135-b12bd8b7d760
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSecurityDescriptor, GetSecurityDescriptor method [Task Scheduler], GetSecurityDescriptor method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetSecurityDescriptor method, ITaskFolder.GetSecurityDescriptor, ITaskFolder::GetSecurityDescriptor, taskschd.itaskfolder_getsecuritydescriptor, taskschd/ITaskFolder::GetSecurityDescriptor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskFolder.GetSecurityDescriptor
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskFolder::GetSecurityDescriptor


## -description


Gets the security descriptor for the folder.


## -parameters




### -param securityInformation [in]

The security information from <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>.


### -param pSddl [out]

The security descriptor for the folder.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9c8ebfdb-3c23-4fec-9023-7a944d99a409">IRegisteredTask::SetSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/54f8a37b-87ac-449c-8e03-aeacd27e8c97">ITaskFolder::SetSecurityDescriptor</a>
 

 

