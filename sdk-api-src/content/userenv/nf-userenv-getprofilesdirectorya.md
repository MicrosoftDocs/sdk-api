---
UID: NF:userenv.GetProfilesDirectoryA
title: GetProfilesDirectoryA function
author: windows-driver-content
description: Retrieves the path to the root directory where user profiles are stored.
old-location: shell\GetProfilesDirectory.htm
old-project: shell
ms.assetid: e21411fa-f7e1-4944-93ce-7d9314d79fbf
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetProfilesDirectory, GetProfilesDirectory function [Windows Shell], GetProfilesDirectoryA, GetProfilesDirectoryW, _shell_GetProfilesDirectory, shell.GetProfilesDirectory, userenv/GetProfilesDirectory, userenv/GetProfilesDirectoryA, userenv/GetProfilesDirectoryW
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
req.unicode-ansi: GetProfilesDirectoryW (Unicode) and GetProfilesDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	GetProfilesDirectory
-	GetProfilesDirectoryA
-	GetProfilesDirectoryW
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# GetProfilesDirectoryA function


## -description


Retrieves the path to the root directory where user profiles are stored.


## -parameters




### -param lpProfileDir

TBD


### -param lpcchSize [in, out]

Type: <b>LPDWORD</b>

Specifies the size of the <i>lpProfilesDir</i> buffer, in <b>TCHARs</b>.
    
                        

If the buffer specified by <i>lpProfilesDir</i> is not large enough or <i>lpProfilesDir</i> is <b>NULL</b>, the function fails and this parameter receives the necessary buffer size, including the terminating null character.


#### - lpProfilesDir [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path to the profiles directory. Set this value to <b>NULL</b> to determine the required size of the buffer.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The following is an example of the path returned by <b>GetProfilesDirectory</b> in Windows XP:

<pre class="syntax" xml:space="preserve"><code>C:\Documents and Settings</code></pre>
The following is an example of the path returned by <b>GetProfilesDirectory</b> in Windows 7:

<pre class="syntax" xml:space="preserve"><code>C:\Users</code></pre>
To obtain the paths of subdirectories of this directory, use the <a href="https://msdn.microsoft.com/a240abc0-e0a6-4f95-8e74-7dc410970212">SHGetFolderPath</a> (Windows XP and earlier) or <a href="https://msdn.microsoft.com/5434c744-484b-4c34-9a76-dddbcb81eb29">SHGetKnownFolderPath</a> (Windows Vista) function.




## -see-also




<a href="https://msdn.microsoft.com/bd08947a-df57-4dd9-b9ba-a01b315bfdf1">GetAllUsersProfileDirectory</a>



<a href="https://msdn.microsoft.com/14ff99cb-838a-442b-9f51-414bd7c0a2ef">GetDefaultUserProfileDirectory</a>



<a href="https://msdn.microsoft.com/b5de762d-c9ee-42b0-bce0-e74bcc9c78f0">GetUserProfileDirectory</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

