---
UID: NF:userenv.ExpandEnvironmentStringsForUserW
title: ExpandEnvironmentStringsForUserW function (userenv.h)
author: windows-sdk-content
description: Expands the source string by using the environment block established for the specified user.
old-location: shell\ExpandEnvironmentStringsForUser.htm
tech.root: shell
ms.assetid: d32fa6c8-035a-4c84-b210-5366f21b6c17
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExpandEnvironmentStringsForUser, ExpandEnvironmentStringsForUser function [Windows Shell], ExpandEnvironmentStringsForUserA, ExpandEnvironmentStringsForUserW, _shell_ExpandEnvironmentStringsForUser, shell.ExpandEnvironmentStringsForUser, userenv/ExpandEnvironmentStringsForUser, userenv/ExpandEnvironmentStringsForUserA, userenv/ExpandEnvironmentStringsForUserW
ms.topic: function
f1_keywords: 
 - "userenv/ExpandEnvironmentStringsForUser"
dev_langs:
 - c++
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExpandEnvironmentStringsForUserW (Unicode) and ExpandEnvironmentStringsForUserA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - ExpandEnvironmentStringsForUser
 - ExpandEnvironmentStringsForUserA
 - ExpandEnvironmentStringsForUserW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExpandEnvironmentStringsForUserW function


## -description


Expands the source string by using the environment block established for the specified user.


## -parameters




### -param hToken [in, optional]

Type: <b>HANDLE</b>

Token for the user, returned from the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. The token must have TOKEN_IMPERSONATE and TOKEN_QUERY access. In addition, as of Windows 7 the token must also have TOKEN_DUPLICATE access. For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.



If <i>hToken</i> is <b>NULL</b>, the environment block contains system variables only.


### -param lpSrc [in]

Type: <b>LPCTSTR</b>

Pointer to the null-terminated source string to be expanded.


### -param lpDest [out]

Type: <b>LPTSTR</b>

Pointer to a buffer that receives the expanded strings.


### -param dwSize [in]

Type: <b>DWORD</b>

Specifies the size of the <i>lpDest</i> buffer, in <b>TCHARs</b>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The following is an example source string:


```
%USERPROFILE%\ntuser.dat
```


When <b>ExpandEnvironmentStringsForUser</b> returns, the destination string expands as follows:


```
C:\Documents and Settings\UserName\ntuser.dat
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
 

 

