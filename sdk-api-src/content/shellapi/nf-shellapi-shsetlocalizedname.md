---
UID: NF:shellapi.SHSetLocalizedName
title: SHSetLocalizedName function (shellapi.h)
description: Sets the localized name of a file in a Shell folder.
helpviewer_keywords: ["SHSetLocalizedName","SHSetLocalizedName function [Windows Shell]","_shell_SHSetLocalizedName","_shell_SHSetLocalizedName_cpp","shell.SHSetLocalizedName","shellapi/SHSetLocalizedName"]
old-location: shell\SHSetLocalizedName.htm
tech.root: shell
ms.assetid: 35b83fc8-3dad-4f08-a3fe-ce047b2ca3a2
ms.date: 12/05/2018
ms.keywords: SHSetLocalizedName, SHSetLocalizedName function [Windows Shell], _shell_SHSetLocalizedName, _shell_SHSetLocalizedName_cpp, shell.SHSetLocalizedName, shellapi/SHSetLocalizedName
req.header: shellapi.h
req.include-header: 
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
req.dll: Shell32.dll; Shell32.dll (version 5.6 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetLocalizedName
 - shellapi/SHSetLocalizedName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHSetLocalizedName
req.apiset: ext-ms-win-shell-shell32-l1-2-0 (introduced in Windows 8.1)
---

# SHSetLocalizedName function


## -description

Sets the localized name of a file in a Shell folder.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string that specifies the fully qualified path of the target file.

### -param pszResModule [in]

Type: <b>PCWSTR</b>

A pointer to a string resource that specifies the localized version of the file name.

### -param idsRes

Type: <b>int</b>

An integer ID that specifies the localized file name in the string resource.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When this string is set, Explorer displays this string instead of the file name. The path to the file is unchanged.
                
                

Applications can get the display (localized) name with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> with the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN_NORMALDISPLAY</a> flag and the parsing (non-localized) name with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname">IShellItem::GetDisplayName</a> using the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn">SIGDN_DESKTOPABSOLUTEPARSING</a> flag.

Calling <a href="/windows/desktop/api/shellapi/nf-shellapi-shremovelocalizedname">SHRemoveLocalizedName</a> makes the display name identical to the parsing name.
