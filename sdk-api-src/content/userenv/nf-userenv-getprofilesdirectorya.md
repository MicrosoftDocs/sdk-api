---
UID: NF:userenv.GetProfilesDirectoryA
title: GetProfilesDirectoryA function (userenv.h)
description: Retrieves the path to the root directory where user profiles are stored. (ANSI)
helpviewer_keywords: ["GetProfilesDirectoryA", "userenv/GetProfilesDirectoryA"]
old-location: shell\GetProfilesDirectory.htm
tech.root: shell
ms.assetid: e21411fa-f7e1-4944-93ce-7d9314d79fbf
ms.date: 12/05/2018
ms.keywords: GetProfilesDirectory, GetProfilesDirectory function [Windows Shell], GetProfilesDirectoryA, GetProfilesDirectoryW, _shell_GetProfilesDirectory, shell.GetProfilesDirectory, userenv/GetProfilesDirectory, userenv/GetProfilesDirectoryA, userenv/GetProfilesDirectoryW
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetProfilesDirectoryW (Unicode) and GetProfilesDirectoryA (ANSI)
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
 - GetProfilesDirectoryA
 - userenv/GetProfilesDirectoryA
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
 - GetProfilesDirectory
 - GetProfilesDirectoryA
 - GetProfilesDirectoryW
---

# GetProfilesDirectoryA function


## -description

Retrieves the path to the root directory where user profiles are stored.

## -parameters

### -param lpProfileDir [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the profiles directory. Set this value to <b>NULL</b> to determine the required size of the buffer.

### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfilesDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfilesDir</i> is not large enough or <i>lpProfilesDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following is an example of the path returned by <b>GetProfilesDirectory</b> in Windows XP:


``` syntax
C:\Documents and Settings
```

The following is an example of the path returned by <b>GetProfilesDirectory</b> in Windows 7:


``` syntax
C:\Users
```

To obtain the paths of subdirectories of this directory, use the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> (Windows XP and earlier) or <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> (Windows Vista) function.





> [!NOTE]
> The userenv.h header defines GetProfilesDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-getallusersprofiledirectorya">GetAllUsersProfileDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getdefaultuserprofiledirectorya">GetDefaultUserProfileDirectory</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getuserprofiledirectorya">GetUserProfileDirectory</a>



<a href="/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
