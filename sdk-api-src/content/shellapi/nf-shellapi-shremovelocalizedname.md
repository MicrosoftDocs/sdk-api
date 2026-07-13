---
UID: NF:shellapi.SHRemoveLocalizedName
title: SHRemoveLocalizedName function (shellapi.h)
description: Removes the localized name of a file in a Shell folder.
helpviewer_keywords: ["SHRemoveLocalizedName","SHRemoveLocalizedName function [Windows Shell]","_shell_SHRemoveLocalizedName","shell.SHRemoveLocalizedName","shellapi/SHRemoveLocalizedName"]
old-location: shell\SHRemoveLocalizedName.htm
tech.root: shell
ms.assetid: ed30546f-3531-42df-9018-1a24a79a0b79
ms.date: 12/05/2018
ms.keywords: SHRemoveLocalizedName, SHRemoveLocalizedName function [Windows Shell], _shell_SHRemoveLocalizedName, shell.SHRemoveLocalizedName, shellapi/SHRemoveLocalizedName
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRemoveLocalizedName
 - shellapi/SHRemoveLocalizedName
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
 - SHRemoveLocalizedName
---

# SHRemoveLocalizedName function


## -description

Removes the localized name of a file in a Shell folder.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string that specifies the fully qualified path of the target file.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a display name string is set by <a href="/windows/desktop/api/shellapi/nf-shellapi-shsetlocalizedname">SHSetLocalizedName</a>, Windows Explorer uses that string for display instead of the file name. The path to the file is unchanged.

Applications can use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> method to get the display (localized) name through with the SIGDN_NORMALDISPLAY flag and the parsing (non-localized) name with SIGDN_DESKTOPABSOLUTEPARSING.

Calling <b>SHRemoveLocalizedName</b> makes the display name identical to the parsing name.