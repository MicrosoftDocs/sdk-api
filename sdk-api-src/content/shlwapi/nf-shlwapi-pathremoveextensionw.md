---
UID: NF:shlwapi.PathRemoveExtensionW
title: PathRemoveExtensionW function
author: windows-sdk-content
description: Removes the file name extension from a path, if one is present.
old-location: shell\PathRemoveExtension.htm
tech.root: shell
ms.assetid: 6e26d005-50af-4376-b734-19ba3d9c470f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: PathRemoveExtension, PathRemoveExtension function [Windows Shell], PathRemoveExtensionA, PathRemoveExtensionW, _win32_PathRemoveExtension, shell.PathRemoveExtension, shlwapi/PathRemoveExtension, shlwapi/PathRemoveExtensionA, shlwapi/PathRemoveExtensionW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathRemoveExtensionW (Unicode) and PathRemoveExtensionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-legacy-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - PathRemoveExtension
 - PathRemoveExtensionA
 - PathRemoveExtensionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathRemoveExtensionW function


## -description


Removes the file name extension from a path, if one is present.
        
            
<div class="alert"><b>Note</b>  This function is deprecated. We recommend the use of the <a href="https://msdn.microsoft.com/9adfb054-6d62-41bb-9036-0bf670ea24b2">PathCchRemoveExtension</a> in its place.</div><div> </div>

## -parameters




### -param pszPath [in, out]

Type: <b>LPTSTR</b>

A pointer to a null-terminated string of length MAX_PATH from which to remove the extension.


## -returns



This function does not return a value.



