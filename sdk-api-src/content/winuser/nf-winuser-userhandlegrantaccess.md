---
UID: NF:winuser.UserHandleGrantAccess
title: UserHandleGrantAccess function (winuser.h)
description: Grants or denies access to a handle to a User object to a job that has a user-interface restriction.
helpviewer_keywords: ["UserHandleGrantAccess","UserHandleGrantAccess function","_win32_userhandlegrantaccess","base.userhandlegrantaccess","winuser/UserHandleGrantAccess"]
old-location: base\userhandlegrantaccess.htm
tech.root: backup
ms.assetid: 6e7a6cfc-f881-43cc-a5af-b97e0bf14bf4
ms.date: 12/05/2018
ms.keywords: UserHandleGrantAccess, UserHandleGrantAccess function, _win32_userhandlegrantaccess, base.userhandlegrantaccess, winuser/UserHandleGrantAccess
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UserHandleGrantAccess
 - winuser/UserHandleGrantAccess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - UserHandleGrantAccess
---

# UserHandleGrantAccess function


## -description

Grants or denies access to a handle to a User object to a job that has a user-interface restriction. When access is granted, all processes associated with the job can subsequently recognize and use the handle. When access is denied, the processes can no longer use the handle. For more information see 
<a href="/windows/desktop/SysInfo/user-objects">User Objects</a>.

## -parameters

### -param hUserHandle [in]

A handle to the User object.

### -param hJob [in]

A handle to the job to be granted access to the User handle. The 
<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a> function returns this handle.

### -param bGrant [in]

If this parameter is TRUE, all processes associated with the job can recognize and use the handle. If the parameter is FALSE, the processes cannot use the handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>UserHandleGrantAccess</b> function can be called only from a process not associated with the job specified by the <i>hJob</i> parameter. The User handle must not be owned by a process or thread associated with the job.

To create user-interface restrictions, call the 
<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> function with the JobObjectBasicUIRestrictions job information class.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a>



<a href="/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>