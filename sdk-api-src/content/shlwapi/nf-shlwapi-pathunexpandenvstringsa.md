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

# PathUnExpandEnvStringsA function


## -description


Replaces certain folder names in a fully qualified path with their associated environment string.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path to be unexpanded.


### -param pszBuf [out]

Type: <b>LPTSTR</b>

A pointer to a buffer that, when this method returns successfully, receives the unexpanded string. The size of this buffer must be set to MAX_PATH to ensure that it is large enough to hold the returned string.


### -param cchBuf [in]

Type: <b>UINT</b>

The size, in characters, in the <i>pszBuf</i> buffer.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.




## -remarks



The following folder paths are replaced by their equivalent environment string.

<table class="clsStd">
<tr>
<th>Folder</th>
<th>Environment String</th>
</tr>
<tr>
<td>The All Users profile folder</td>
<td>%ALLUSERSPROFILE%</td>
</tr>
<tr>
<td>The current user's application data folder (Windows Vista and later only).</td>
<td>%APPDATA%</td>
</tr>
<tr>
<td>The system name</td>
<td>%COMPUTERNAME%</td>
</tr>
<tr>
<td>The Program Files folder</td>
<td>%ProgramFiles%</td>
</tr>
<tr>
<td>The system root folder</td>
<td>%SystemRoot%</td>
</tr>
<tr>
<td>The system drive letter</td>
<td>%SystemDrive%</td>
</tr>
<tr>
<td>The current user's profile folder</td>
<td>%USERPROFILE%</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  %APPDATA% and %USERPROFILE% are relative to the user making the call. This function does not work if the user is being impersonated from a service. For further discussion of access control issues, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>.</div>
<div> </div>
The environment variables listed in the above table might not all be set on all systems. If an environment variable is not set, it is not unexpanded.




## -see-also




<a href="https://msdn.microsoft.com/cdf8bf2d-f446-4e0d-8664-bff2c45f74ec">DoEnvironmentSubst</a>
 

 

