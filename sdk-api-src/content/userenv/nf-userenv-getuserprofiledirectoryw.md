---
UID: NF:userenv.GetUserProfileDirectoryW
title: GetUserProfileDirectoryW function (userenv.h)
description: Retrieves the path to the root directory of the specified user's profile. (Unicode)
helpviewer_keywords: ["GetUserProfileDirectory", "GetUserProfileDirectory function [Windows Shell]", "GetUserProfileDirectoryW", "_shell_GetUserProfileDirectory", "shell.GetUserProfileDirectory", "userenv/GetUserProfileDirectory", "userenv/GetUserProfileDirectoryW"]
old-location: shell\GetUserProfileDirectory.htm
tech.root: shell
ms.assetid: b5de762d-c9ee-42b0-bce0-e74bcc9c78f0
ms.date: 12/05/2018
ms.keywords: GetUserProfileDirectory, GetUserProfileDirectory function [Windows Shell], GetUserProfileDirectoryA, GetUserProfileDirectoryW, _shell_GetUserProfileDirectory, shell.GetUserProfileDirectory, userenv/GetUserProfileDirectory, userenv/GetUserProfileDirectoryA, userenv/GetUserProfileDirectoryW
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetUserProfileDirectoryW (Unicode) and GetUserProfileDirectoryA (ANSI)
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
 - GetUserProfileDirectoryW
 - userenv/GetUserProfileDirectoryW
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
 - GetUserProfileDirectory
 - GetUserProfileDirectoryA
 - GetUserProfileDirectoryW
---

# GetUserProfileDirectoryW function


## -description

Retrieves the path to the root directory of the specified user's profile.

## -parameters

### -param hToken [in]

Type: <b>HANDLE</b>

A token for the user, which is returned by the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or  <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. The token must have TOKEN_QUERY access. For more information, see <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param lpProfileDir [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the specified user's profile directory.

### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfileDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfileDir</i> is not large enough or <i>lpProfileDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.

If the function succeeds then this parameter receives the number of <b>TCHARs</b> written to <i>lpProfileDir</i>, including the terminating null character.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows XP:


``` syntax
C:\Documents and Settings\Joe
```

The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows 7:


``` syntax
C:\Users\Joe
```

To obtain the paths of subdirectories of this directory, use the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> (Windows XP and earlier) or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> (Windows Vista) function.





> [!NOTE]
> The userenv.h header defines GetUserProfileDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-getallusersprofiledirectorya">GetAllUsersProfileDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getdefaultuserprofiledirectorya">GetDefaultUserProfileDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getprofilesdirectorya">GetProfilesDirectory</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
