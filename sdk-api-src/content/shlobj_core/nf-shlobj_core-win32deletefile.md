---
UID: NF:shlobj_core.Win32DeleteFile
title: Win32DeleteFile function
author: windows-sdk-content
description: Win32DeleteFile may be altered or unavailable.
old-location: shell\Win32DeleteFile.htm
tech.root: shell
ms.assetid: e6b2ac77-a206-413e-aba7-0fd627799a95
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: Win32DeleteFile, Win32DeleteFile function [Windows Shell], _shell_Win32DeleteFile, shell.Win32DeleteFile, shlobj_core/Win32DeleteFile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Shell32.dll
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
 - Win32DeleteFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Win32DeleteFile function


## -description


<p class="CCE_Message">[<b>Win32DeleteFile</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Deletes a file.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a buffer that contains the full name of the file to delete.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the file was successfully deleted; otherwise <b>FALSE</b>.



