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

# SHRegGetPathW function


## -description


Retrieves a file path from the registry, expanding environment variables as needed.


## -parameters




### -param hKey

TBD


### -param pcszSubKey

TBD


### -param pcszValue

TBD


### -param pszPath [out]

Type: <b>LPTSTR</b>

A buffer to hold the expanded path. You should set the size of this buffer to <b>MAX_PATH</b> to ensure that it is large enough to hold the returned string.


### -param dwFlags

Type: <b>DWORD</b>

Reserved.


#### - hkey [in]

Type: <b>HKEY</b>

A handle to a key that is currently open, or a registry root key.


#### - pszSubkey [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the name of the subkey.


#### - pszValue [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the name of the value that holds the unexpanded path string.


## -returns



Type: <b>LSTATUS</b>

Returns <b>ERROR_SUCCESS</b> if successful, or a Windows error code otherwise.




## -remarks



The data type of the specified registry value must be either <b>REG_EXPAND_SZ</b> or <b>REG_SZ</b>. If it has the <b>REG_EXPAND_SZ</b> type, any environment variables in the registry string will be expanded with <a href="https://msdn.microsoft.com/b563e8ed-311d-4971-94f3-9c9fde4a2f30">ExpandEnvironmentStrings</a>. If it has the <b>REG_SZ</b> data type, environment variables will not be expanded and the string pointed to by <i>pszPath</i> will be identical to the string in the registry.

The following environment strings will be replaced by their equivalent path.

<table class="clsStd">
<tr>
<th>Environment string</th>
<th>Folder</th>
</tr>
<tr>
<td>
							%USERPROFILE%
						</td>
<td>The current user's profile folder</td>
</tr>
<tr>
<td>
							%ALLUSERSPROFILE%
						</td>
<td>The All Users profile folder</td>
</tr>
<tr>
<td>
							%ProgramFiles%
						</td>
<td>The Program Files folder</td>
</tr>
<tr>
<td>
							%SystemRoot%
						</td>
<td>The system root folder</td>
</tr>
<tr>
<td>
							%SystemDrive%
						</td>
<td>The system drive letter</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %USERPROFILE% is relative to the user making the call. This function does not work if the user is being impersonated from a service.</div>
<div> </div>


