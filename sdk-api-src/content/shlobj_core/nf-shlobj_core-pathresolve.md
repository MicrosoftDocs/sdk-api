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

# PathResolve function


## -description


<p class="CCE_Message">[<b>PathResolve</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Converts a relative or unqualified path name to a fully qualified path name.


## -parameters




### -param pszPath [in, out]

Type: <b>PWSTR</b>

A null-terminated Unicode string that contains the path to resolve. When the function returns, the string contains the corresponding fully qualified path. This buffer should be at least MAX_PATH characters long.


### -param dirs [in, optional]

Type: <b>PZPCWSTR</b>

A pointer to an optional null-terminated array of directories to be searched first in the case that the path cannot be resolved from <i>pszPath</i>. This value can be <b>NULL</b>.


### -param fFlags

Type: <b>UINT</b>

Flags that specify how the function operates.



#### PRF_VERIFYEXISTS

Return <b>TRUE</b> if the file's existence is verified; otherwise <b>FALSE</b>.



#### PRF_TRYPROGRAMEXTENSIONS

Look for the specified path with the following extensions appended: .pif, .com, .bat, .cmd, .lnk, and .exe.



#### PRF_FIRSTDIRDEF

Look first in the directory or directories specified by <i>dirs</i>.



#### PRF_DONTFINDLNK

Ignore .lnk files.



#### PRF_REQUIREABSOLUTE

Require an absolute (full) path.


## -returns



Type: <b>int</b>

Returns <b>TRUE</b>, unless PRF_VERIFYEXISTS is set. If that flag is set, the function returns <b>TRUE</b> if the file is verified to exist and <b>FALSE</b> otherwise. It also sets an ERROR_FILE_NOT_FOUND error code that you can retrieve by calling <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A <b>FALSE</b> return value does not necessarily mean that the file does not exist. It might mean that the function is simply unable to find the file from the supplied information.

If <b>PathResolve</b> cannot resolve the path specified in <i>pszPath</i>, it calls <a href="https://msdn.microsoft.com/d9281eb2-39b7-444f-85b7-1e1e76c38ae2">PathFindOnPath</a> using <i>pszPath</i> and <i>dirs</i> as the parameters.




## -see-also




<a href="https://msdn.microsoft.com/d9281eb2-39b7-444f-85b7-1e1e76c38ae2">PathFindOnPath</a>
 

 

