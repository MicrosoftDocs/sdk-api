---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SHRegSetPathA function


## -description


Takes a file path, replaces folder names with environment strings, and places the resulting string in the registry.


## -parameters




### -param hKey

TBD


### -param pcszSubKey

TBD


### -param pcszValue

TBD


### -param pcszPath

TBD


### -param dwFlags

Type: <b>DWORD</b>

Reserved.


#### - hkey [in]

Type: <b>HKEY</b>

A handle to a key that is currently open, or a registry root key.


#### - pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with a fully qualified file path.


#### - pszSubkey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the name of an existing subkey. If the subkey does not exist, <b>SHRegSetPath</b> will fail.


#### - pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string with the name of the value to hold the path string.


## -returns



Type: <b>LSTATUS</b>

Returns ERROR_SUCCESS if successful, or a Windows error code otherwise.




## -remarks



For Windows 2000, <b>SHRegSetPath</b> uses <a href="https://msdn.microsoft.com/cfab1ee0-03f3-4e0f-a29d-5331fec022b5">PathUnExpandEnvStrings</a> to convert folder names to their corresponding environment string. If any environment variables were substituted, the registry value will be set with the <b>REG_EXPAND_SZ</b> data type. Otherwise, it will be set with the <b>REG_SZ</b> data type.

The following folder paths will be replaced by their equivalent environment string.

<table class="clsStd">
<tr>
<th>Folder</th>
<th>Environment string</th>
</tr>
<tr>
<td>The current user's profile folder</td>
<td>
							%USERPROFILE%
						</td>
</tr>
<tr>
<td>The All Users profile folder</td>
<td>
							%ALLUSERSPROFILE%
						</td>
</tr>
<tr>
<td>The Program Files folder</td>
<td>
							%ProgramFiles%
						</td>
</tr>
<tr>
<td>The system root folder</td>
<td>
							%SystemRoot%
						</td>
</tr>
<tr>
<td>The system drive letter</td>
<td>
							%SystemDrive%
						</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %USERPROFILE% is relative to the user making the call. This function does not work if the user is being impersonated from a service.</div>
<div> </div>
The environment variables listed in the above table might not all be set on any particular system. If an environment variable is not set, it will not be unexpanded. In particular, none of these variables are set for the default environment of Windows 95 or Windows 98. The %ProgramFiles% variable is new for Windows 2000, and will typically not be set on Microsoft Windows NT 4.0 systems.



