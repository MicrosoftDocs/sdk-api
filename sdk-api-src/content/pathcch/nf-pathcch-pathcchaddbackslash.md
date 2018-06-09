---
UID: NF:pathcch.PathCchAddBackslash
title: PathCchAddBackslash function
author: windows-sdk-content
description: Adds a backslash to the end of a string to create the correct syntax for a path.
old-location: shell\PathCchAddBackslash.htm
old-project: shell
ms.assetid: b50677cd-8815-4d84-b70a-c83863378c56
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: PathCchAddBackslash, PathCchAddBackslash function [Windows Shell], pathcch/PathCchAddBackslash, shell.PathCchAddBackslash
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - pathcch.lib
 - API-MS-Win-Core-Path-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PathCchAddBackslash
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PathCchAddBackslash function


## -description



Adds a backslash to the end of a string to create the correct syntax for a path. If the source path already has a trailing backslash, no backslash will be added.

This function differs from <b>PathCchAddBackslash</b> in that you are restricted to a final path of length MAX_PATH.

This function differs from <a href="https://msdn.microsoft.com/27d8aec7-8b00-412a-9a42-8ce27e262781">PathAddBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, or <a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a>, should be used in place of <a href="https://msdn.microsoft.com/27d8aec7-8b00-412a-9a42-8ce27e262781">PathAddBackslash</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the buffer contains the string with the appended backslash. This value should not be <b>NULL</b>.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the function was successful, S_FALSE if the path string already ends in a backslash, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/89adf45f-f16d-49d1-9e76-b57b73b4d4c3">PathCchAddBackslashEx</a>
 

 

