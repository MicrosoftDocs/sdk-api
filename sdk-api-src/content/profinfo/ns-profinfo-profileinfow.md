---
UID: NS:profinfo._PROFILEINFOW
title: PROFILEINFOW
author: windows-sdk-content
description: Contains information used when loading or unloading a user profile.
old-location: shell\PROFILEINFO.htm
tech.root: shell
ms.assetid: 09dae38c-3b2b-4f12-9c1e-90737cf0c7cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPROFILEINFOW, LPPROFILEINFO, LPPROFILEINFO structure pointer [Windows Shell], PI_APPLYPOLICY, PI_NOUI, PROFILEINFO, PROFILEINFO structure [Windows Shell], PROFILEINFOA, PROFILEINFOW, _shell_PROFILEINFO, profinfo/LPPROFILEINFO, profinfo/PROFILEINFO, profinfo/PROFILEINFOA, profinfo/PROFILEINFOW, shell.PROFILEINFO"
ms.topic: struct
req.header: profinfo.h
req.include-header: Userenv.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROFILEINFOW (Unicode) and PROFILEINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Profinfo.h
api_name:
 - PROFILEINFO
 - PROFILEINFOA
 - PROFILEINFOW
product: Windows
targetos: Windows
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
req.redist: 
---

# PROFILEINFOW structure


## -description


Contains information used when loading or unloading a user profile.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field dwFlags

Type: <b>DWORD</b>

This member can be one of the following flags:



#### PI_NOUI

Prevents the display of profile error messages.



#### PI_APPLYPOLICY

Not supported.


### -field lpUserName

Type: <b>LPTSTR</b>

A pointer to the name of the user. This member is used as the base name of the directory in which to store a new profile.


### -field lpProfilePath

Type: <b>LPTSTR</b>

A pointer to the <a href="https://msdn.microsoft.com/8af06fdf-be99-4295-8f11-7d7f68e66956">roaming user profile</a> path. If the user does not have a roaming profile, this member can be <b>NULL</b>. To retrieve the user's roaming profile path, call the <a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a> function, specifying information level 3 or 4. For more information, see Remarks.


### -field lpDefaultPath

Type: <b>LPTSTR</b>

A pointer to the default user profile path. This member can be <b>NULL</b>.


### -field lpServerName

Type: <b>LPTSTR</b>

A pointer to the name of the validating domain controller, in NetBIOS format.


### -field lpPolicyPath

Type: <b>LPTSTR</b>

Not used, set to <b>NULL</b>.


### -field hProfile

Type: <b>HANDLE</b>

A handle to the <b>HKEY_CURRENT_USER</b> registry subtree. For more information, see Remarks.


##### - dwFlags.PI_APPLYPOLICY

Not supported.


##### - dwFlags.PI_NOUI

Prevents the display of profile error messages.


## -remarks



Do not use environment variables when specifying a path. The 
<a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> function does not expand environment variables, such as %username%, in a path.

When the <a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> call returns successfully, the <b>hProfile</b> member receives a registry key handle opened to the root of the user's subtree, opened with full access (KEY_ALL_ACCESS). For more information see the Remarks sections in <b>LoadUserProfile</b>, 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>, and 
<a href="https://msdn.microsoft.com/fe517d88-7b03-4dc3-b3db-6a92665bca8e">Registry Hives</a>.

Services and applications that call <a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> should check to see if the user has a roaming profile. If the user has a roaming profile, specify its path as the <b>lpProfilePath</b> member of this structure.




## -see-also




<a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a>



<a href="https://msdn.microsoft.com/7ecb8a3f-c041-4133-b23a-101de8884882">UnloadUserProfile</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>
 

 

