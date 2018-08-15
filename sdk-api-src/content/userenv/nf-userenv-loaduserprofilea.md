---
UID: NF:userenv.LoadUserProfileA
title: LoadUserProfileA function
author: windows-sdk-content
description: Loads the specified user's profile. The profile can be a local user profile or a roaming user profile.
old-location: shell\LoadUserProfile.htm
old-project: shell
ms.assetid: 9ec1f8f2-8f20-4d38-9d41-70315b890336
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LoadUserProfile, LoadUserProfile function [Windows Shell], LoadUserProfileA, LoadUserProfileW, _shell_LoadUserProfile, shell.LoadUserProfile, userenv/LoadUserProfile, userenv/LoadUserProfileA, userenv/LoadUserProfileW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: userenv.h
req.include-header: 
req.redist: 
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
 - LoadUserProfile
 - LoadUserProfileA
 - LoadUserProfileW
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# LoadUserProfileA function


## -description


Loads the specified user's profile. The profile can be a 
<a href="https://msdn.microsoft.com/0e6c060e-025e-4d00-9b92-4f3b7bf66dda">local user profile</a> or a 
<a href="https://msdn.microsoft.com/8af06fdf-be99-4295-8f11-7d7f68e66956">roaming user profile</a>.


## -parameters




### -param hToken [in]

Type: <b>HANDLE</b>

Token for the user, which is returned by the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, <a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, <a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, <a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or <a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function. The token must have <b>TOKEN_QUERY</b>, <b>TOKEN_IMPERSONATE</b>, and <b>TOKEN_DUPLICATE</b> access. For more information, see <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param lpProfileInfo [in, out]

Type: <b>LPPROFILEINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a> structure. <b>LoadUserProfile</b> fails and returns <b>ERROR_INVALID_PARAMETER</b> if the <b>dwSize</b> member of the structure is not set to <code>sizeof(PROFILEINFO)</code> or if the <b>lpUserName</b> member is <b>NULL</b>. For more information, see Remarks.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
                
                    

The function fails and returns ERROR_INVALID_PARAMETER if the <b>dwSize</b> member of the structure at <i>lpProfileInfo</i> is not set to <code>sizeof(PROFILEINFO)</code> or if the <b>lpUserName</b> member is <b>NULL</b>.




## -remarks



When a user logs on interactively, the system automatically loads the user's profile. If a service or an application impersonates a user, the system does not load the user's profile. Therefore, the service or application should load the user's profile with <b>LoadUserProfile</b>.

Services and applications that call <b>LoadUserProfile</b> should check to see if the user has a roaming profile. If the user has a roaming profile, specify its path as the <b>lpProfilePath</b> member of 
<a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a>. To retrieve the user's roaming profile path, you can call the 
<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a> function, specifying information level 3 or 4.

Upon successful return, the <b>hProfile</b> member of <a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a> is a registry key handle opened to the root of the user's hive. It has been opened with full access (KEY_ALL_ACCESS). If a service that is impersonating a user needs to read or write to the user's registry file, use this handle instead of <b>HKEY_CURRENT_USER</b>. Do not close the <b>hProfile</b> handle. Instead, pass it to the 
<a href="https://msdn.microsoft.com/7ecb8a3f-c041-4133-b23a-101de8884882">UnloadUserProfile</a> function. This function closes the handle. You should ensure that all handles to keys in the user's registry hive are closed. If you do not close all open registry handles, the user's profile fails to unload. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a> and <a href="https://msdn.microsoft.com/fe517d88-7b03-4dc3-b3db-6a92665bca8e">Registry Hives</a>.

Note that it is your responsibility to load the user's registry hive into the <b>HKEY_USERS</b> registry key with the <b>LoadUserProfile</b> function before you call <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>. This is because <b>CreateProcessAsUser</b> does not load the specified user's profile into <b>HKEY_USERS</b>. This means that access to information in the <b>HKEY_CURRENT_USER</b> registry key may not produce results consistent with a normal interactive logon.

The calling process must have the <b>SE_RESTORE_NAME</b> and <b>SE_BACKUP_NAME</b> privileges. For more information, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

Starting with Windows XP Service Pack 2 (SP2) and Windows Server 2003, the caller must be an administrator or the LocalSystem account. It is not sufficient for the caller to merely impersonate the administrator or LocalSystem account.




## -see-also




<a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a>



<a href="https://msdn.microsoft.com/7ecb8a3f-c041-4133-b23a-101de8884882">UnloadUserProfile</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

