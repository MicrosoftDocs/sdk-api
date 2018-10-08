---
UID: NF:winuser.UserHandleGrantAccess
title: UserHandleGrantAccess function
author: windows-sdk-content
description: Grants or denies access to a handle to a User object to a job that has a user-interface restriction.
old-location: base\userhandlegrantaccess.htm
tech.root: procthread
ms.assetid: 6e7a6cfc-f881-43cc-a5af-b97e0bf14bf4
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: UserHandleGrantAccess, UserHandleGrantAccess function, _win32_userhandlegrantaccess, base.userhandlegrantaccess, winuser/UserHandleGrantAccess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - UserHandleGrantAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UserHandleGrantAccess function


## -description


Grants or denies access to a handle to a User object to a job that has a user-interface restriction. When access is granted, all processes associated with the job can subsequently recognize and use the handle. When access is denied, the processes can no longer use the handle. For more information see 
<a href="https://msdn.microsoft.com/07edc049-26d9-4f42-a5e7-e1f4c8435a6c">User Objects</a>.


## -parameters




### -param hUserHandle [in]

A handle to the User object.


### -param hJob [in]

A handle to the job to be granted access to the User handle. The 
<a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> or 
<a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a> function returns this handle.


### -param bGrant [in]

If this parameter is TRUE, all processes associated with the job can recognize and use the handle. If the parameter is FALSE, the processes cannot use the handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>UserHandleGrantAccess</b> function can be called only from a process not associated with the job specified by the <i>hJob</i> parameter. The User handle must not be owned by a process or thread associated with the job.

To create user-interface restrictions, call the 
<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a> function with the JobObjectBasicUIRestrictions job information class.




## -see-also




<a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

