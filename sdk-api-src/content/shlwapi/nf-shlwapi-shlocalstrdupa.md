---
UID: NF:shlwapi.SHLocalStrDupA
title: SHLocalStrDupA function
author: windows-sdk-content
description: Makes a copy of a string in newly allocated memory.
old-location: shell\SHLocalStrDup.htm
tech.root: shell
ms.assetid: 79da6160-b1b1-41c3-9b21-229aadf251dd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SHLocalStrDup, SHLocalStrDup function [Windows Shell], SHLocalStrDupA, SHLocalStrDupW, _shell_SHLocalStrDup, shell.SHLocalStrDup, shlwapi/SHLocalStrDup, shlwapi/SHLocalStrDupA, shlwapi/SHLocalStrDupW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHLocalStrDupW (Unicode) and SHLocalStrDupA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - SHLocalStrDup
 - SHLocalStrDupA
 - SHLocalStrDupW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHLocalStrDupA function


## -description


Makes a copy of a string in newly allocated memory.


## -parameters




### -param psz

Type: <b>PCTSTR</b>

A pointer to a null-terminated, Unicode string to be copied.


### -param ppsz [out, optional]

Type: <b>PTSTR*</b>

The address of a pointer to an allocated string that, when this function returns successfully, receives the result. <b>SHLocalStrDup</b> allocates memory for this string with <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>. You should free the string with <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



