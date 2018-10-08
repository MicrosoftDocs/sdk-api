---
UID: NF:shlwapi.SHRegDeleteUSValueW
title: SHRegDeleteUSValueW function
author: windows-sdk-content
description: Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegDeleteUSValue.htm
tech.root: shell
ms.assetid: f70407af-d8ee-4333-be32-01887d4add4c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SHRegDeleteUSValue, SHRegDeleteUSValue function [Windows Shell], SHRegDeleteUSValueA, SHRegDeleteUSValueW, _win32_SHRegDeleteUSValue, shell.SHRegDeleteUSValue, shlwapi/SHRegDeleteUSValue, shlwapi/SHRegDeleteUSValueA, shlwapi/SHRegDeleteUSValueW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHRegDeleteUSValueW (Unicode) and SHRegDeleteUSValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-Registryuserspecific-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - SHRegDeleteUSValue
 - SHRegDeleteUSValueA
 - SHRegDeleteUSValueW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHRegDeleteUSValueW function


## -description


Deletes a registry subkey value in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


#### - pwzValue [in]

Type: <b>LPCTSTR</b>

A pointer to the null-terminated string that names the value to remove.


### -param delRegFlags [in]

Type: <b><a href="https://msdn.microsoft.com/90a8bf22-f62b-4027-8219-7a5ead6577da">SHREGDEL_FLAGS</a></b>

One of the <a href="https://msdn.microsoft.com/90a8bf22-f62b-4027-8219-7a5ead6577da">SHREGDEL_FLAGS</a> that specifies from which base key the value will be deleted.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. You can use the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.




## -see-also




<a href="https://msdn.microsoft.com/adb09a2b-674c-472d-9f16-8e150476f1f5">SHRegDeleteEmptyUSKey</a>
 

 

