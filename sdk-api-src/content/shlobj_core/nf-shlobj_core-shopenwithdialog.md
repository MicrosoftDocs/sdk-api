---
UID: NF:shlobj_core.SHOpenWithDialog
title: SHOpenWithDialog function
author: windows-sdk-content
description: Displays the Open With dialog box.
old-location: shell\SHOpenWithDialog.htm
old-project: shell
ms.assetid: 026bfb34-a8a5-4bd7-9bc0-4aa395e6d535
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SHOpenWithDialog, SHOpenWithDialog function [Windows Shell], _shell_SHOpenWithDialog, shell.SHOpenWithDialog, shlobj_core/SHOpenWithDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - SHOpenWithDialog
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# SHOpenWithDialog function


## -description


Displays the <b>Open With</b> dialog box.


## -parameters




### -param hwndParent [in, optional]

Type: <b>HWND</b>

The handle of the parent window. This value can be <b>NULL</b>.


### -param poainfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/5486c4d3-c6c5-459d-aa7f-426971184876">OPENASINFO</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/5486c4d3-c6c5-459d-aa7f-426971184876">OPENASINFO</a> structure, which specifies the contents of the resulting dialog.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Starting in Windows 10, the <b>OAIF_ALLOW_REGISTRATION</b>, <b>OAIF_FORCE_REGISTRATION</b>, and <b>OAIF_HIDE_REGISTRATION</b> flags will be ignored by <b>SHOpenWithDialog</b>. The <b>Open With</b> dialog box can no longer be used to change the default program used to open a file extension. You can only use <b>SHOpenWithDialog</b> to open a single file.

If <b>SHOpenWithDialog</b> is called without passing <b>OAIF_EXEC</b>, the user will receive a dialog that informs them that they can change the default programs used to open file extensions in their <b>Settings</b>.



