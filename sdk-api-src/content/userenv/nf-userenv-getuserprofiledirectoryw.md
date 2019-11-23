---
UID: NF:userenv.GetUserProfileDirectoryW
title: GetUserProfileDirectoryW function (userenv.h)

description: Retrieves the path to the root directory of the specified user's profile.
old-location: shell\GetUserProfileDirectory.htm
tech.root: shell
ms.assetid: b5de762d-c9ee-42b0-bce0-e74bcc9c78f0

ms.date: 12/05/2018
ms.keywords: GetUserProfileDirectory, GetUserProfileDirectory function [Windows Shell], GetUserProfileDirectoryA, GetUserProfileDirectoryW, _shell_GetUserProfileDirectory, shell.GetUserProfileDirectory, userenv/GetUserProfileDirectory, userenv/GetUserProfileDirectoryA, userenv/GetUserProfileDirectoryW
ms.topic: function
f1_keywords: 
 - "userenv/GetUserProfileDirectory"
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
req.unicode-ansi: GetUserProfileDirectoryW (Unicode) and GetUserProfileDirectoryA (ANSI)
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
 - GetUserProfileDirectory
 - GetUserProfileDirectoryA
 - GetUserProfileDirectoryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetUserProfileDirectoryW function


## -description


Retrieves the path to the root directory of the specified user's profile.


## -parameters




### -param hToken [in]

Type: <b>HANDLE</b>

A token for the user, which is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or  <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. The token must have TOKEN_QUERY access. For more information, see <a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.


### -param lpProfileDir [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the specified user's profile directory.


### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfileDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfileDir</i> is not large enough or <i>lpProfileDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows XP:

<pre class="syntax" xml:space="preserve"><code>C:\Documents and Settings\Joe</code></pre>
The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows 7:

<pre class="syntax" xml:space="preserve"><code>C:\Users\Joe</code></pre>
To obtain the paths of subdirectories of this directory, use the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">SHGetFolderPath</a> (Windows XP and earlier) or <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath">SHGetKnownFolderPath</a> (Windows Vista) function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getallusersprofiledirectorya">GetAllUsersProfileDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getdefaultuserprofiledirectorya">GetDefaultUserProfileDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getprofilesdirectorya">GetProfilesDirectory</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776900(v=vs.85)">User Profiles Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb776901(v=vs.85)">User Profiles Reference</a>
 

 

