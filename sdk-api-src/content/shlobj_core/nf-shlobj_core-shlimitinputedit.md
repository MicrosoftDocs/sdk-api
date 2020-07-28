---
UID: NF:shlobj_core.SHLimitInputEdit
title: SHLimitInputEdit function (shlobj_core.h)
description: Sets limits on valid characters for an edit control.
helpviewer_keywords: ["SHLimitInputEdit","SHLimitInputEdit function [Windows Shell]","_shell_SHLimitInputEdit","shell.SHLimitInputEdit","shlobj_core/SHLimitInputEdit"]
old-location: shell\SHLimitInputEdit.htm
tech.root: shell
ms.assetid: 3f03374f-8dfe-4b80-9ecc-12c6548f2865
ms.date: 12/05/2018
ms.keywords: SHLimitInputEdit, SHLimitInputEdit function [Windows Shell], _shell_SHLimitInputEdit, shell.SHLimitInputEdit, shlobj_core/SHLimitInputEdit
f1_keywords:
- shlobj_core/SHLimitInputEdit
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
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
- SHLimitInputEdit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHLimitInputEdit function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Sets limits on valid characters for an edit control.


## -parameters




### -param hwndEdit [in, optional]

Type: <b>HWND</b>

The handle of the edit control.


### -param psf [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

An <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface pointer. This object must also implement <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits">IItemNameLimits</a>, which supplies a list of invalid characters and a maximum name length.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



