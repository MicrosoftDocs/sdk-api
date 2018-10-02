---
UID: NF:shlobj_core.PathYetAnotherMakeUniqueName
title: PathYetAnotherMakeUniqueName function
author: windows-sdk-content
description: Creates a unique filename based on an existing filename.
old-location: shell\PathYetAnotherMakeUniqueName.htm
tech.root: Shell
ms.assetid: 1f76ecfa-6f2f-4dde-b05e-4252c92660d9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PathYetAnotherMakeUniqueName, PathYetAnotherMakeUniqueName function [Windows Shell], _win32_PathYetAnotherMakeUniqueName, shell.PathYetAnotherMakeUniqueName, shlobj_core/PathYetAnotherMakeUniqueName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - PathYetAnotherMakeUniqueName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathYetAnotherMakeUniqueName function


## -description


Creates a unique filename based on an existing filename.


## -parameters




### -param pszUniqueName [out]

Type: <b>PWSTR</b>

A string buffer that receives a null-terminated Unicode string that contains the fully qualified path of the unique file name. This buffer should be at least MAX_PATH characters long to avoid causing a buffer overrun.


### -param pszPath [in]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the fully qualified path of folder that will contain the new file. If <i>pszShort</i> is set to <b>NULL</b>, this string must contain a full destination path, ending with the long file name that the new file name will be base on.


### -param pszShort [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the short file name that the unique name will be based on. Set this value to <b>NULL</b> to create a name based on the long file name.


### -param pszFileSpec [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that contains the long file name that the unique name will be based on.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if a unique name was successfully created; otherwise <b>FALSE</b>.




## -remarks



If the generated path exceeds MAX_PATH characters, this function may return a truncated string in <b>PathYetAnotherMakeUniqueName</b>. In that case, the function returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/8456ae0c-e83c-43d0-a86a-1861a373d237">PathMakeUniqueName</a>
 

 

