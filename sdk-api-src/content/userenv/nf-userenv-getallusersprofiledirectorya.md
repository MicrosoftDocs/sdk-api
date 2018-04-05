---
UID: NF:userenv.GetAllUsersProfileDirectoryA
title: GetAllUsersProfileDirectoryA function
author: windows-driver-content
description: Retrieves the path to the root of the directory that contains program data shared by all users.
old-location: shell\GetAllUsersProfileDirectory.htm
old-project: shell
ms.assetid: bd08947a-df57-4dd9-b9ba-a01b315bfdf1
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetAllUsersProfileDirectory, GetAllUsersProfileDirectory function [Windows Shell], GetAllUsersProfileDirectoryA, GetAllUsersProfileDirectoryW, _shell_GetAllUsersProfileDirectory, shell.GetAllUsersProfileDirectory, userenv/GetAllUsersProfileDirectory, userenv/GetAllUsersProfileDirectoryA, userenv/GetAllUsersProfileDirectoryW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SOFTDISTINFO, *LPSOFTDISTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	GetAllUsersProfileDirectory
-	GetAllUsersProfileDirectoryA
-	GetAllUsersProfileDirectoryW
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
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

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following is an example of the path returned by <b>GetAllUsersProfileDirectory</b> in Windows XP:

<pre class="syntax" xml:space="preserve"><code>C:\Documents and Settings\All Users</code></pre>
The following is an example of the path returned by <b>GetAllUsersProfileDirectory</b> in Windows 7:

<pre class="syntax" xml:space="preserve"><code>C:\ProgramData</code></pre>
To obtain the paths of subdirectories of this directory, use the <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a> (Windows XP and earlier) or <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a> (Windows Vista) function.




## -see-also




<a href="https://msdn.microsoft.com/14ff99cb-838a-442b-9f51-414bd7c0a2ef">GetDefaultUserProfileDirectory</a>



<a href="https://msdn.microsoft.com/e21411fa-f7e1-4944-93ce-7d9314d79fbf">GetProfilesDirectory</a>



<a href="https://msdn.microsoft.com/b5de762d-c9ee-42b0-bce0-e74bcc9c78f0">GetUserProfileDirectory</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

