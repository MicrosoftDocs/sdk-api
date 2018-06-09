---
UID: NF:pathcch.PathCchRemoveExtension
title: PathCchRemoveExtension function
author: windows-sdk-content
description: Removes the file name extension from a path, if one is present.This function differs from PathRemoveExtension in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchRemoveExtension.htm
old-project: shell
ms.assetid: 9adfb054-6d62-41bb-9036-0bf670ea24b2
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: PathCchRemoveExtension, PathCchRemoveExtension function [Windows Shell], pathcch/PathCchRemoveExtension, shell.PathCchRemoveExtension
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
 - PathCchRemoveExtension
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PathCchRemoveExtension function


## -description



Removes the file name extension from a path, if one is present.

This function differs from <a href="https://msdn.microsoft.com/6e26d005-50af-4376-b734-19ba3d9c470f">PathRemoveExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function, should be used in place of <a href="https://msdn.microsoft.com/6e26d005-50af-4376-b734-19ba3d9c470f">PathRemoveExtension</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the string contains the path with any extension removed. If no extension was found, the string is unchanged.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the function was successful, S_FALSE if no extension was found, or an error code otherwise.



