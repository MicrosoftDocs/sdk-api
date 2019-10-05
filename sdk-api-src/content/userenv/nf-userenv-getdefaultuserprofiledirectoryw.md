---
UID: NF:userenv.GetDefaultUserProfileDirectoryW
title: GetDefaultUserProfileDirectoryW function (userenv.h)
author: windows-sdk-content
description: Retrieves the path to the root of the default user's profile.
old-location: shell\GetDefaultUserProfileDirectory.htm
tech.root: shell
ms.assetid: 14ff99cb-838a-442b-9f51-414bd7c0a2ef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDefaultUserProfileDirectory, GetDefaultUserProfileDirectory function [Windows Shell], GetDefaultUserProfileDirectoryA, GetDefaultUserProfileDirectoryW, _shell_GetDefaultUserProfileDirectory, shell.GetDefaultUserProfileDirectory, userenv/GetDefaultUserProfileDirectory, userenv/GetDefaultUserProfileDirectoryA, userenv/GetDefaultUserProfileDirectoryW
ms.topic: function
f1_keywords: 
 - "userenv/GetDefaultUserProfileDirectory"
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
req.unicode-ansi: GetDefaultUserProfileDirectoryW (Unicode) and GetDefaultUserProfileDirectoryA (ANSI)
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
 - GetDefaultUserProfileDirectory
 - GetDefaultUserProfileDirectoryA
 - GetDefaultUserProfileDirectoryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDefaultUserProfileDirectoryW function


## -description


Retrieves the path to the root of the default user's profile.


## -parameters




### -param lpProfileDir [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the default user's profile directory. Set this value to <b>NULL</b> to determine the required size of the buffer.


### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfileDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfileDir</i> is not large enough or <i>lpProfileDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The following is an example of the path returned by <b>GetDefaultUserProfileDirectory</b> in Windows XP:

<pre class="syntax" xml:space="preserve"><code>C:\Documents and Settings\Default User</code></pre>
The following is an example of the path returned by <b>GetDefaultUserProfileDirectory</b> in Windows 7:

<pre class="syntax" xml:space="preserve"><code>C:\Users\Default</code></pre>
To obtain the paths of subdirectories of this directory, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> (Windows XP and earlier) or <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> (Windows Vista) function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getallusersprofiledirectorya">GetAllUsersProfileDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getprofilesdirectorya">GetProfilesDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getuserprofiledirectorya">GetUserProfileDirectory</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
 

 

