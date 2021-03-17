---
UID: NF:userenv.UnloadUserProfile
title: UnloadUserProfile function (userenv.h)
description: Unloads a user's profile that was loaded by the LoadUserProfile function. The caller must have administrative privileges on the computer. For more information, see the Remarks section of the LoadUserProfile function.
helpviewer_keywords: ["UnloadUserProfile","UnloadUserProfile function [Windows Shell]","_shell_UnloadUserProfile","shell.UnloadUserProfile","userenv/UnloadUserProfile"]
old-location: shell\UnloadUserProfile.htm
tech.root: shell
ms.assetid: 7ecb8a3f-c041-4133-b23a-101de8884882
ms.date: 12/05/2018
ms.keywords: UnloadUserProfile, UnloadUserProfile function [Windows Shell], _shell_UnloadUserProfile, shell.UnloadUserProfile, userenv/UnloadUserProfile
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
 - UnloadUserProfile
 - userenv/UnloadUserProfile
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
 - UnloadUserProfile
---

# UnloadUserProfile function


## -description

Unloads a user's profile that was loaded by the <a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> function. The caller must have administrative privileges on the computer. For more information, see the Remarks section of the <b>LoadUserProfile</b> function.

## -parameters

### -param hToken [in]

Type: <b>HANDLE</b>

Token for the user, returned from the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. The token must have <b>TOKEN_IMPERSONATE</b> and <b>TOKEN_DUPLICATE</b> access. For more information, see <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param hProfile [in]

Type: <b>HANDLE</b>

Handle to the registry key. This value is the <b>hProfile</b> member of the <a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a> structure. For more information see the Remarks section of <a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a> and <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Before calling <b>UnloadUserProfile</b> you should ensure that all handles to keys that you have opened in the user's registry hive are closed. If you do not close all open registry handles, the user's profile fails to unload. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a> and <a href="/windows/desktop/SysInfo/registry-hives">Registry Hives</a>.

For more information about calling functions that require administrator privileges, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-loaduserprofilea">LoadUserProfile</a>



<a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>