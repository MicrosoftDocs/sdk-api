---
UID: NF:userenv.CreateEnvironmentBlock
title: CreateEnvironmentBlock function (userenv.h)
description: Retrieves the environment variables for the specified user. This block can then be passed to the CreateProcessAsUser function.
helpviewer_keywords: ["CreateEnvironmentBlock","CreateEnvironmentBlock function [Windows Shell]","_shell_CreateEnvironmentBlock","shell.CreateEnvironmentBlock","userenv/CreateEnvironmentBlock"]
old-location: shell\CreateEnvironmentBlock.htm
tech.root: shell
ms.assetid: bda8879d-d33a-48f4-8b08-e3a279126a07
ms.date: 12/05/2018
ms.keywords: CreateEnvironmentBlock, CreateEnvironmentBlock function [Windows Shell], _shell_CreateEnvironmentBlock, shell.CreateEnvironmentBlock, userenv/CreateEnvironmentBlock
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateEnvironmentBlock
 - userenv/CreateEnvironmentBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - CreateEnvironmentBlock
---

# CreateEnvironmentBlock function


## -description

Retrieves the environment variables for the specified user. This block can then be passed to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function.

## -parameters

### -param lpEnvironment [out]

Type: <b>LPVOID*</b>

When this function returns, receives a pointer to the new environment block. The environment block is an array of null-terminated Unicode strings. The list ends with two nulls (\0\0).

### -param hToken [in, optional]

Type: <b>HANDLE</b>

Token for the user, returned from the 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function. If this is a primary token, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_DUPLICATE</b> access. If the token is an impersonation token, it must have <b>TOKEN_QUERY</b> access. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>. 

                    

If this parameter is <b>NULL</b>, the returned environment block contains system variables only.

### -param bInherit [in]

Type: <b>BOOL</b>

Specifies whether to inherit from the current process' environment. If this value is <b>TRUE</b>, the process inherits the current process' environment. If this value is <b>FALSE</b>, the process does not inherit the current process' environment.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To free the buffer when you have finished with the environment block, call the 
<a href="/windows/desktop/api/userenv/nf-userenv-destroyenvironmentblock">DestroyEnvironmentBlock</a> function.

If the environment block is passed to 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>, you must also specify the <b>CREATE_UNICODE_ENVIRONMENT</b> flag. After <b>CreateProcessAsUser</b> has returned, the new process has a copy of the environment block, and <a href="/windows/desktop/api/userenv/nf-userenv-destroyenvironmentblock">DestroyEnvironmentBlock</a> can be safely called.

User-specific environment variables such as %USERPROFILE% are set only when the user's profile is loaded. To load a user's profile, call the 
<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> function.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/userenv/nf-userenv-destroyenvironmentblock">DestroyEnvironmentBlock</a>



<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>