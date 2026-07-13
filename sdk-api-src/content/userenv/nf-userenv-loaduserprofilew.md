---
UID: NF:userenv.LoadUserProfileW
title: LoadUserProfileW function (userenv.h)
description: Loads the specified user's profile. The profile can be a local user profile or a roaming user profile. (Unicode)
helpviewer_keywords: ["LoadUserProfile", "LoadUserProfile function [Windows Shell]", "LoadUserProfileW", "_shell_LoadUserProfile", "shell.LoadUserProfile", "userenv/LoadUserProfile", "userenv/LoadUserProfileW"]
old-location: shell\LoadUserProfile.htm
tech.root: shell
ms.assetid: 9ec1f8f2-8f20-4d38-9d41-70315b890336
ms.date: 12/05/2018
ms.keywords: LoadUserProfile, LoadUserProfile function [Windows Shell], LoadUserProfileA, LoadUserProfileW, _shell_LoadUserProfile, shell.LoadUserProfile, userenv/LoadUserProfile, userenv/LoadUserProfileA, userenv/LoadUserProfileW
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadUserProfileW (Unicode) and LoadUserProfileA (ANSI)
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
 - LoadUserProfileW
 - userenv/LoadUserProfileW
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
 - LoadUserProfile
 - LoadUserProfileA
 - LoadUserProfileW
---

# LoadUserProfileW function


## -description

Loads the specified user's profile. The profile can be a 
<a href="/previous-versions/windows/desktop/legacy/bb776894(v=vs.85)">local user profile</a> or a 
<a href="/previous-versions/windows/desktop/legacy/bb776897(v=vs.85)">roaming user profile</a>.

## -parameters

### -param hToken [in]

Type: <b>HANDLE</b>

Token for the user, which is returned by the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. The token must have <b>TOKEN_QUERY</b>, <b>TOKEN_IMPERSONATE</b>, and <b>TOKEN_DUPLICATE</b> access. For more information, see <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param lpProfileInfo [in, out]

Type: <b>LPPROFILEINFO</b>

Pointer to a <a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a> structure. <b>LoadUserProfile</b> fails and returns <b>ERROR_INVALID_PARAMETER</b> if the <b>dwSize</b> member of the structure is not set to <code>sizeof(PROFILEINFO)</code> or if the <b>lpUserName</b> member is <b>NULL</b>. For more information, see Remarks.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
                
                    

The function fails and returns ERROR_INVALID_PARAMETER if the <b>dwSize</b> member of the structure at <i>lpProfileInfo</i> is not set to <code>sizeof(PROFILEINFO)</code> or if the <b>lpUserName</b> member is <b>NULL</b>.

## -remarks

When a user logs on interactively, the system automatically loads the user's profile. If a service or an application impersonates a user, the system does not load the user's profile. Therefore, the service or application should load the user's profile with <b>LoadUserProfile</b>.

Services and applications that call <b>LoadUserProfile</b> should check to see if the user has a roaming profile. If the user has a roaming profile, specify its path as the <b>lpProfilePath</b> member of 
<a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a>. To retrieve the user's roaming profile path, you can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netusergetinfo">NetUserGetInfo</a> function, specifying information level 3 or 4.

Upon successful return, the <b>hProfile</b> member of <a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a> is a registry key handle opened to the root of the user's hive. It has been opened with full access (KEY_ALL_ACCESS). If a service that is impersonating a user needs to read or write to the user's registry file, use this handle instead of <b>HKEY_CURRENT_USER</b>. Do not close the <b>hProfile</b> handle. Instead, pass it to the 
<a href="/windows/desktop/api/userenv/nf-userenv-unloaduserprofile">UnloadUserProfile</a> function. This function closes the handle. You should ensure that all handles to keys in the user's registry hive are closed. If you do not close all open registry handles, the user's profile fails to unload. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a> and <a href="/windows/desktop/SysInfo/registry-hives">Registry Hives</a>.

Note that it is your responsibility to load the user's registry hive into the <b>HKEY_USERS</b> registry key with the <b>LoadUserProfile</b> function before you call <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>. This is because <b>CreateProcessAsUser</b> does not load the specified user's profile into <b>HKEY_USERS</b>. This means that access to information in the <b>HKEY_CURRENT_USER</b> registry key may not produce results consistent with a normal interactive logon.

The calling process must have the <b>SE_RESTORE_NAME</b> and <b>SE_BACKUP_NAME</b> privileges. For more information, see <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Starting with Windows XP Service Pack 2 (SP2) and Windows Server 2003, the caller must be an administrator or the LocalSystem account. It is not sufficient for the caller to merely impersonate the administrator or LocalSystem account.





> [!NOTE]
> The userenv.h header defines LoadUserProfile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/profinfo/ns-profinfo-profileinfoa">PROFILEINFO</a>



<a href="/windows/desktop/api/userenv/nf-userenv-unloaduserprofile">UnloadUserProfile</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
