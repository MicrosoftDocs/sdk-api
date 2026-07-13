---
UID: NF:userenv.GetAllUsersProfileDirectoryA
title: GetAllUsersProfileDirectoryA function (userenv.h)
description: Retrieves the path to the root of the directory that contains program data shared by all users. (ANSI)
helpviewer_keywords: ["GetAllUsersProfileDirectoryA", "userenv/GetAllUsersProfileDirectoryA"]
old-location: shell\GetAllUsersProfileDirectory.htm
tech.root: shell
ms.assetid: bd08947a-df57-4dd9-b9ba-a01b315bfdf1
ms.date: 12/05/2018
ms.keywords: GetAllUsersProfileDirectory, GetAllUsersProfileDirectory function [Windows Shell], GetAllUsersProfileDirectoryA, GetAllUsersProfileDirectoryW, _shell_GetAllUsersProfileDirectory, shell.GetAllUsersProfileDirectory, userenv/GetAllUsersProfileDirectory, userenv/GetAllUsersProfileDirectoryA, userenv/GetAllUsersProfileDirectoryW
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAllUsersProfileDirectoryW (Unicode) and GetAllUsersProfileDirectoryA (ANSI)
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
 - GetAllUsersProfileDirectoryA
 - userenv/GetAllUsersProfileDirectoryA
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
 - GetAllUsersProfileDirectory
 - GetAllUsersProfileDirectoryA
 - GetAllUsersProfileDirectoryW
---

# GetAllUsersProfileDirectoryA function


## -description

Retrieves the path to the root of the directory that contains program data shared by all users.

## -parameters

### -param lpProfileDir [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path. Set this value to <b>NULL</b> to determine the required size of the buffer, including the terminating null character.

### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

A pointer to the size of the <i>lpProfileDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfileDir</i> is not large enough or <i>lpProfileDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following is an example of the path returned by <b>GetAllUsersProfileDirectory</b> in Windows XP:


``` syntax
C:\Documents and Settings\All Users
```

The following is an example of the path returned by <b>GetAllUsersProfileDirectory</b> in Windows 7:


``` syntax
C:\ProgramData
```

To obtain the paths of subdirectories of this directory, use the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> (Windows XP and earlier) or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> (Windows Vista) function.





> [!NOTE]
> The userenv.h header defines GetAllUsersProfileDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-getdefaultuserprofiledirectorya">GetDefaultUserProfileDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getprofilesdirectorya">GetProfilesDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getuserprofiledirectorya">GetUserProfileDirectory</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
