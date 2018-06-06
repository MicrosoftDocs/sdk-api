---
UID: NF:userenv.GetUserProfileDirectoryW
title: GetUserProfileDirectoryW function
author: windows-sdk-content
description: Retrieves the path to the root directory of the specified user's profile.
old-location: shell\GetUserProfileDirectory.htm
old-project: shell
ms.assetid: b5de762d-c9ee-42b0-bce0-e74bcc9c78f0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetUserProfileDirectory, GetUserProfileDirectory function [Windows Shell], GetUserProfileDirectoryA, GetUserProfileDirectoryW, _shell_GetUserProfileDirectory, shell.GetUserProfileDirectory, userenv/GetUserProfileDirectory, userenv/GetUserProfileDirectoryA, userenv/GetUserProfileDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
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
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# GetUserProfileDirectoryW function


## -description


Retrieves the path to the root directory of the specified user's profile.


## -parameters




### -param hToken [in]

Type: <b>HANDLE</b>

A token for the user, which is returned by the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, <a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, <a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, <a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or  <a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function. The token must have TOKEN_QUERY access. For more information, see <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param lpProfileDir [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the specified user's profile directory.


### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfileDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfileDir</i> is not large enough or <i>lpProfileDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows XP:

<pre class="syntax" xml:space="preserve"><code>C:\Documents and Settings\Joe</code></pre>
The following is an example of the path returned by <b>GetUserProfileDirectory</b> in Windows 7:

<pre class="syntax" xml:space="preserve"><code>C:\Users\Joe</code></pre>
To obtain the paths of subdirectories of this directory, use the <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a> (Windows XP and earlier) or <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a> (Windows Vista) function.




## -see-also




<a href="https://msdn.microsoft.com/bd08947a-df57-4dd9-b9ba-a01b315bfdf1">GetAllUsersProfileDirectory</a>



<a href="https://msdn.microsoft.com/14ff99cb-838a-442b-9f51-414bd7c0a2ef">GetDefaultUserProfileDirectory</a>



<a href="https://msdn.microsoft.com/e21411fa-f7e1-4944-93ce-7d9314d79fbf">GetProfilesDirectory</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

