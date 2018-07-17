---
UID: NF:shlobj_core.Shell_GetCachedImageIndexW
title: Shell_GetCachedImageIndexW function
author: windows-sdk-content
description: Shell_GetCachedImageIndex may be altered or unavailable.
old-location: shell\Shell_GetCachedImageIndex.htm
old-project: shell
ms.assetid: f0d4dd1f-a41c-4dd0-9713-e3aec48ff101
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Shell_GetCachedImageIndex, Shell_GetCachedImageIndex function [Windows Shell], Shell_GetCachedImageIndexA, Shell_GetCachedImageIndexW, _win32_Shell_GetCachedImageIndex, shell.Shell_GetCachedImageIndex, shlobj_core/Shell_GetCachedImageIndex, shlobj_core/Shell_GetCachedImageIndexA, shlobj_core/Shell_GetCachedImageIndexW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h, Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Shell_GetCachedImageIndexW (Unicode) and Shell_GetCachedImageIndexA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
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
 - Shell_GetCachedImageIndex
 - Shell_GetCachedImageIndexA
 - Shell_GetCachedImageIndexW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Shell_GetCachedImageIndexW function


## -description


<p class="CCE_Message">[<b>Shell_GetCachedImageIndex</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <b>Shell_GetCachedImageIndexA</b> or <b>Shell_GetCachedImageIndexW</b>.]

Retrieves the cache index of a cached icon.


## -parameters




### -param pszIconPath

TBD


### -param iIconIndex

Type: <b>int</b>

The index of the image within the file named at <i>pwszIconPath</i>.


### -param uIconFlags

Type: <b>UINT</b>

Not used.


#### - pwszIconPath [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the path to the image file.


## -returns



Type: <b>int</b>

Returns the index of the image, or –1 on failure.




## -remarks



The <b>Shell_GetCachedImageIndexA</b> and <b>Shell_GetCachedImageIndexW</b> versions of this function were added in Windows Vista. For Unicode strings, call either <b>Shell_GetCachedImageIndexW</b> or <b>Shell_GetCachedImageIndex</b>. For ANSI strings, you must call <b>Shell_GetCachedImageIndexA</b> explicitly.

<b>Windows Server 2003 and Windows XP:  </b>Only <b>Shell_GetCachedImageIndex</b> is supported. <b>Shell_GetCachedImageIndex</b> requires a Unicode string.




## -see-also




<a href="https://msdn.microsoft.com/4e661326-157e-4c75-86df-cd213e01c3e5">FileIconInit</a>
 

 

