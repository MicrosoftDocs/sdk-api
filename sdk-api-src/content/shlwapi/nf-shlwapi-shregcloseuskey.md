---
UID: NF:shlwapi.SHRegCloseUSKey
title: SHRegCloseUSKey function (shlwapi.h)
description: Closes a handle to a user-specific registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).
helpviewer_keywords: ["SHRegCloseUSKey","SHRegCloseUSKey function [Windows Shell]","_win32_SHRegCloseUSKey","shell.SHRegCloseUSKey","shlwapi/SHRegCloseUSKey"]
old-location: shell\SHRegCloseUSKey.htm
tech.root: shell
ms.assetid: 1e9900d6-8411-4e6b-a9c0-006f378a2625
ms.date: 12/05/2018
ms.keywords: SHRegCloseUSKey, SHRegCloseUSKey function [Windows Shell], _win32_SHRegCloseUSKey, shell.SHRegCloseUSKey, shlwapi/SHRegCloseUSKey
req.header: shlwapi.h
req.include-header: 
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegCloseUSKey
 - shlwapi/SHRegCloseUSKey
dev_langs:
 - c++
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
---

# SHRegCloseUSKey function


## -description

Closes a handle to a user-specific registry subkey in a user-specific subtree (HKEY_CURRENT_USER or HKEY_LOCAL_MACHINE).

## -parameters

### -param hUSKey [in]

Type: <b>HUSKEY</b>

A handle to a currently open registry subkey. The subkey must have been opened with the KEY_SET_VALUE access right. For more information, see <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

                        

This handle can be obtained through the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya">SHRegOpenUSKey</a> function.

## -returns

Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a nonzero error code defined in Winerror.h otherwise. Use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> with the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.