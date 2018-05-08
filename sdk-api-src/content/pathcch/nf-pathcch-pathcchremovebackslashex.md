---
UID: NF:pathcch.PathCchRemoveBackslashEx
title: PathCchRemoveBackslashEx function
author: windows-driver-content
description: Removes the trailing backslash from the end of a path string.This function differs from PathCchRemoveBackslash in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.This function differs from PathRemoveBackslash in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchRemoveBackslashEx.htm
old-project: shell
ms.assetid: 250c2faa-94bb-42c1-97d4-37f8f59dbde6
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: PathCchRemoveBackslashEx, PathCchRemoveBackslashEx function [Windows Shell], pathcch/PathCchRemoveBackslashEx, shell.PathCchRemoveBackslashEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	pathcch.lib
-	API-MS-Win-Core-Path-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PathCchRemoveBackslashEx
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PathCchRemoveBackslashEx function


## -description



Removes the trailing backslash from the end of a path string.

This function differs from <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a> in that it can return a pointer to the new end of the string and report the number of unused characters remaining in the buffer.

This function differs from <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, or <a href="https://msdn.microsoft.com/61afc20e-ee6c-46ad-a058-64c57de41ba4">PathCchRemoveBackslash</a>, should be used in place of <a href="https://msdn.microsoft.com/58d13c38-40aa-4aaa-81dc-2b68425f1fe0">PathRemoveBackslash</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any trailing backslash removed. If no trailing backslash was found, the string is unchanged.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param ppszEnd [out, optional]

A value that, when this function returns successfully, receives the address of a pointer to end of the new string. If the string is a root path such as "C:\", the pointer points to the backslash; otherwise the pointer points to the string's terminating null character.


### -param pcchRemaining [out, optional]

A pointer to a value that, when this function returns successfully, receives the number of unused characters in the destination buffer, including the terminating null character. If the string is a root path such as "C:\", this count includes the backslash in that string.


## -returns



This function returns S_OK if the function was successful, S_FALSE if the string was a root path or if no backslash was found, or an error code otherwise.




## -remarks



This function will not remove the backslash from a root path string, such as "C:\".



