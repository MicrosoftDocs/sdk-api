---
UID: NF:shlobj_core.PathGetShortPath
title: PathGetShortPath function
author: windows-sdk-content
description: PathGetShortPath may be altered or unavailable.
old-location: shell\PathGetShortPath.htm
old-project: shell
ms.assetid: f374a575-3fbf-4bed-aa76-76ed81e01d60
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: PathGetShortPath, PathGetShortPath function [Windows Shell], _win32_PathGetShortPath, shell.PathGetShortPath, shlobj_core/PathGetShortPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - PathGetShortPath
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# PathGetShortPath function


## -description


<p class="CCE_Message">[<b>PathGetShortPath</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves the short path form of a specified input path.


## -parameters




### -param pszLongPath [in, out]

Type: <b>PWSTR</b>

A pointer to a null-terminated, Unicode string that contains the long path. When the function returns, it contains the equivalent short path.


## -returns



This function does not return a value.



