---
UID: NF:shlobj_core.SHOpenWithDialog
title: SHOpenWithDialog function (shlobj_core.h)
description: Displays the Open With dialog box.
helpviewer_keywords: ["SHOpenWithDialog","SHOpenWithDialog function [Windows Shell]","_shell_SHOpenWithDialog","shell.SHOpenWithDialog","shlobj_core/SHOpenWithDialog"]
old-location: shell\SHOpenWithDialog.htm
tech.root: shell
ms.assetid: 026bfb34-a8a5-4bd7-9bc0-4aa395e6d535
ms.date: 12/05/2018
ms.keywords: SHOpenWithDialog, SHOpenWithDialog function [Windows Shell], _shell_SHOpenWithDialog, shell.SHOpenWithDialog, shlobj_core/SHOpenWithDialog
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHOpenWithDialog
 - shlobj_core/SHOpenWithDialog
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHOpenWithDialog
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHOpenWithDialog function


## -description

Displays the <b>Open With</b> dialog box.

## -parameters

### -param hwndParent [in, optional]

Type: <b>HWND</b>

The handle of the parent window. This value can be <b>NULL</b>.

### -param poainfo [in]

Type: <b>const <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo">OPENASINFO</a>*</b>

A pointer to an <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo">OPENASINFO</a> structure, which specifies the contents of the resulting dialog.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Starting in Windows 10, the <b>OAIF_ALLOW_REGISTRATION</b>, <b>OAIF_FORCE_REGISTRATION</b>, and <b>OAIF_HIDE_REGISTRATION</b> flags will be ignored by <b>SHOpenWithDialog</b>. The <b>Open With</b> dialog box can no longer be used to change the default program used to open a file extension. You can only use <b>SHOpenWithDialog</b> to open a single file.

If <b>SHOpenWithDialog</b> is called without passing <b>OAIF_EXEC</b>, the user will receive a dialog that informs them that they can change the default programs used to open file extensions in their <b>Settings</b>.
