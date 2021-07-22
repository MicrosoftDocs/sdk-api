---
UID: NF:shlobj_core.SHGetSetFolderCustomSettings
title: SHGetSetFolderCustomSettings function (shlobj_core.h)
description: SHGetSetFolderCustomSettings may be altered or unavailable.
helpviewer_keywords: ["FCS_FORCEWRITE","FCS_READ","FCS_WRITE","SHGetSetFolderCustomSettings","SHGetSetFolderCustomSettings function [Windows Shell]","_win32_SHGetSetFolderCustomSettings","shell.SHGetSetFolderCustomSettings","shlobj_core/SHGetSetFolderCustomSettings"]
old-location: shell\SHGetSetFolderCustomSettings.htm
tech.root: shell
ms.assetid: 38b78a4b-ba68-4dff-812d-d4c7421eb202
ms.date: 12/05/2018
ms.keywords: FCS_FORCEWRITE, FCS_READ, FCS_WRITE, SHGetSetFolderCustomSettings, SHGetSetFolderCustomSettings function [Windows Shell], _win32_SHGetSetFolderCustomSettings, shell.SHGetSetFolderCustomSettings, shlobj_core/SHGetSetFolderCustomSettings
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetSetFolderCustomSettings
 - shlobj_core/SHGetSetFolderCustomSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetSetFolderCustomSettings
---

# SHGetSetFolderCustomSettings function


## -description

<p class="CCE_Message">[<b>SHGetSetFolderCustomSettings</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets or retrieves custom folder settings. This function reads from and writes to Desktop.ini.

## -parameters

### -param pfcs [in, out]

Type: <b>LPSHFOLDERCUSTOMSETTINGS</b>

A pointer to a <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings">SHFOLDERCUSTOMSETTINGS</a> structure that provides or receives the custom folder settings.

### -param pszPath [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated Unicode string that contains the path to the folder. The length of  <b>pszPath</b> must be MAX_PATH or less, including the terminating null character.

### -param dwReadWrite

Type: <b>DWORD</b>

A flag that controls the action of the function. It may be one of the following values.



#### FCS_READ (0x00000001)

Retrieve the custom folder settings in <i>pfcs</i>.



#### FCS_FORCEWRITE (0x00000002)

Use <i>pfcs</i> to set the custom folder's settings regardless of whether the values are already present.



#### FCS_WRITE (FCS_READ | FCS_FORCEWRITE)

Use <i>pfcs</i> to set the custom folder's settings if the values are not already present.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only Unicode strings are supported.

<b>Windows Server 2003 and Windows XP:  </b><b>SHGetSetFolderCustomSettings</b> supports both ANSI and Unicode strings.