---
UID: NF:pathcch.PathCchRemoveBackslash
title: PathCchRemoveBackslash function
author: windows-sdk-content
description: Removes the trailing backslash from the end of a path string.This function differs from PathRemoveBackslash in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchRemoveBackslash.htm
tech.root: shell
ms.assetid: 61afc20e-ee6c-46ad-a058-64c57de41ba4
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PathCchRemoveBackslash, PathCchRemoveBackslash function [Windows Shell], pathcch/PathCchRemoveBackslash, shell.PathCchRemoveBackslash
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pathcch.lib
req.dll: 
req.irql: 
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
 - PathCchRemoveBackslash
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathCchRemoveBackslash function


## -description



Removes the trailing backslash from the end of a path string.

This function differs from <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, or <a href="https://msdn.microsoft.com/250c2faa-94bb-42c1-97d4-37f8f59dbde6">PathCchRemoveBackslashEx</a>, should be used in place of <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any trailing backslash removed. If no trailing backslash was found, the string is unchanged.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the function was successful, S_FALSE if the string was a root path or if no backslash was found, or an error code otherwise.




## -remarks



This function will not remove the backslash from a root path string, such as "C:\".



