---
UID: NF:userenv.CreateEnvironmentBlock
title: CreateEnvironmentBlock function
author: windows-sdk-content
description: Retrieves the environment variables for the specified user. This block can then be passed to the CreateProcessAsUser function.
old-location: shell\CreateEnvironmentBlock.htm
old-project: shell
ms.assetid: bda8879d-d33a-48f4-8b08-e3a279126a07
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateEnvironmentBlock, CreateEnvironmentBlock function [Windows Shell], _shell_CreateEnvironmentBlock, shell.CreateEnvironmentBlock, userenv/CreateEnvironmentBlock
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	CreateEnvironmentBlock
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# CreateEnvironmentBlock function


## -description


Retrieves the environment variables for the specified user. This block can then be passed to the <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function.


## -parameters




### -param lpEnvironment [out]

Type: <b>LPVOID*</b>

When this function returns, receives a pointer to the new environment block. The environment block is an array of null-terminated Unicode strings. The list ends with two nulls (\0\0).


### -param hToken [in, optional]

Type: <b>HANDLE</b>

Token for the user, returned from the 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function. If this is a primary token, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_DUPLICATE</b> access. If the token is an impersonation token, it must have <b>TOKEN_QUERY</b> access. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>. 

                    

If this parameter is <b>NULL</b>, the returned environment block contains system variables only.


### -param bInherit [in]

Type: <b>BOOL</b>

Specifies whether to inherit from the current process' environment. If this value is <b>TRUE</b>, the process inherits the current process' environment. If this value is <b>FALSE</b>, the process does not inherit the current process' environment.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To free the buffer when you have finished with the environment block, call the 
<a href="https://msdn.microsoft.com/8d03e102-3f8a-4aa7-b175-0a6781eedea7">DestroyEnvironmentBlock</a> function.

If the environment block is passed to 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>, you must also specify the <b>CREATE_UNICODE_ENVIRONMENT</b> flag. After <b>CreateProcessAsUser</b> has returned, the new process has a copy of the environment block, and <a href="https://msdn.microsoft.com/8d03e102-3f8a-4aa7-b175-0a6781eedea7">DestroyEnvironmentBlock</a> can be safely called.

User-specific environment variables such as %USERPROFILE% are set only when the user's profile is loaded. To load a user's profile, call the 
<a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/8d03e102-3f8a-4aa7-b175-0a6781eedea7">DestroyEnvironmentBlock</a>



<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

