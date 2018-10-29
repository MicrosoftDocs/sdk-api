---
UID: NF:shlobj_core.SHCreateFileExtractIconW
title: SHCreateFileExtractIconW function
author: windows-sdk-content
description: SHCreateFileExtractIcon may be altered or unavailable.
old-location: shell\SHCreateFileExtractIcon.htm
tech.root: shell
ms.assetid: af3beb0a-892b-43e5-b5b8-8005f497b6e5
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SHCreateFileExtractIcon, SHCreateFileExtractIcon function [Windows Shell], SHCreateFileExtractIconW, _win32_SHCreateFileExtractIcon, shell.SHCreateFileExtractIcon, shlobj_core/SHCreateFileExtractIcon, shlobj_core/SHCreateFileExtractIconW
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
req.unicode-ansi: SHCreateFileExtractIconW (Unicode)
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
api_name:
 - SHCreateFileExtractIcon
 - SHCreateFileExtractIconW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateFileExtractIconW function


## -description


<p class="CCE_Message">[<b>SHCreateFileExtractIcon</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a default <a href="https://msdn.microsoft.com/f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f">IExtractIcon</a> handler for a file system object. Namespace extensions that display file system objects typically use this function. The extension and file attributes derive all that is needed for a simple icon extractor.


## -parameters




### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that specifies the file system object. The buffer must not exceed MAX_PATH characters in length.


### -param dwFileAttributes [in]

Type: <b>DWORD</b>

A combination of one or more file attribute flags (FILE_ATTRIBUTE_* values as defined in Winnt.h) that specify the type of object.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID of the icon extractor interface to create. This must be either IID_IExtractIconA or IID_IExtractIconW.


### -param ppv

Type: <b>void**</b>

When this function returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f">IExtractIcon</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



