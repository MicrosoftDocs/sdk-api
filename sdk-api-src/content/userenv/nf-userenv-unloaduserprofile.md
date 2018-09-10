---
UID: NF:userenv.UnloadUserProfile
title: UnloadUserProfile function
author: windows-sdk-content
description: Unloads a user's profile that was loaded by the LoadUserProfile function. The caller must have administrative privileges on the computer. For more information, see the Remarks section of the LoadUserProfile function.
old-location: shell\UnloadUserProfile.htm
tech.root: shell
ms.assetid: 7ecb8a3f-c041-4133-b23a-101de8884882
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: UnloadUserProfile, UnloadUserProfile function [Windows Shell], _shell_UnloadUserProfile, shell.UnloadUserProfile, userenv/UnloadUserProfile
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
req.unicode-ansi: 
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
 - UnloadUserProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnloadUserProfile function


## -description


Unloads a user's profile that was loaded by the <a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> function. The caller must have administrative privileges on the computer. For more information, see the Remarks section of the <b>LoadUserProfile</b> function.


## -parameters




### -param hToken [in]

Type: <b>HANDLE</b>

Token for the user, returned from the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, <a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, <a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, <a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or <a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function. The token must have <b>TOKEN_IMPERSONATE</b> and <b>TOKEN_DUPLICATE</b> access. For more information, see <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param hProfile [in]

Type: <b>HANDLE</b>

Handle to the registry key. This value is the <b>hProfile</b> member of the <a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a> structure. For more information see the Remarks section of <a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a> and <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if successful; otherwise, <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Before calling <b>UnloadUserProfile</b> you should ensure that all handles to keys that you have opened in the user's registry hive are closed. If you do not close all open registry handles, the user's profile fails to unload. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a> and <a href="https://msdn.microsoft.com/fe517d88-7b03-4dc3-b3db-6a92665bca8e">Registry Hives</a>.

For more information about calling functions that require administrator privileges, see <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.




## -see-also




<a href="https://msdn.microsoft.com/9ec1f8f2-8f20-4d38-9d41-70315b890336">LoadUserProfile</a>



<a href="https://msdn.microsoft.com/09dae38c-3b2b-4f12-9c1e-90737cf0c7cc">PROFILEINFO</a>



<a href="https://msdn.microsoft.com/754c6aa9-b431-4d2b-a78b-c4da59ea8354">User Profiles Overview</a>



<a href="https://msdn.microsoft.com/86871866-bb90-4287-9640-0a6cd136a800">User Profiles Reference</a>
 

 

