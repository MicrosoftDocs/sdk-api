---
UID: NF:shlobj.INewShortcutHookW.GetFolder
title: INewShortcutHookW::GetFolder (shlobj.h)
description: Gets the folder name for the shortcut object. (Unicode)
helpviewer_keywords: ["GetFolder","GetFolder method [Windows Shell]","GetFolder method [Windows Shell]","INewShortcutHook interface","INewShortcutHook interface [Windows Shell]","GetFolder method","INewShortcutHook::GetFolder","INewShortcutHookA","INewShortcutHookA::GetFolder","INewShortcutHookW","INewShortcutHookW.GetFolder","INewShortcutHookW::GetFolder","_win32_INewShortcutHook_GetFolder","shell.INewShortcutHook_GetFolder","shlobj/INewShortcutHook::GetFolder"]
old-location: shell\INewShortcutHook_GetFolder.htm
tech.root: shell
ms.assetid: 2b743242-3ebe-46cb-a084-575228cb314b
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],INewShortcutHook interface, INewShortcutHook interface [Windows Shell],GetFolder method, INewShortcutHook::GetFolder, INewShortcutHookA, INewShortcutHookA::GetFolder, INewShortcutHookW, INewShortcutHookW.GetFolder, INewShortcutHookW::GetFolder, _win32_INewShortcutHook_GetFolder, shell.INewShortcutHook_GetFolder, shlobj/INewShortcutHook::GetFolder
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INewShortcutHookW::GetFolder
 - shlobj/INewShortcutHookW::GetFolder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INewShortcutHook.GetFolder
 - INewShortcutHookA::GetFolder
 - INewShortcutHookW::GetFolder
---

# INewShortcutHookW::GetFolder


## -description

Gets the folder name for the shortcut object.

## -parameters

### -param pszFolder [out]

Type: <b>PTSTR</b>

The address of a character buffer that receives the folder name.

### -param cchFolder

Type: <b>int</b>

The size of the buffer at <i>pszFolder</i>, in characters.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if no folder has been assigned, or a standard error code otherwise.

