---
UID: NF:shlwapi.SHRegCloseUSKey
title: SHRegCloseUSKey function
author: windows-sdk-content
description: Closes a handle to a user-specific registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
old-location: shell\SHRegCloseUSKey.htm
old-project: shell
ms.assetid: 1e9900d6-8411-4e6b-a9c0-006f378a2625
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SHRegCloseUSKey, SHRegCloseUSKey function [Windows Shell], _win32_SHRegCloseUSKey, shell.SHRegCloseUSKey, shlwapi/SHRegCloseUSKey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: URL_SCHEME
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
 - SHRegCloseUSKey
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHRegCloseUSKey function


## -description


Closes a handle to a user-specific registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).


## -parameters




### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="https://msdn.microsoft.com/756430a9-a495-412e-95c3-a93222bc467a">SHRegOpenUSKey</a> function.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.



