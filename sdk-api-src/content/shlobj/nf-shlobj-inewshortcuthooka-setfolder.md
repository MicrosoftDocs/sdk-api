---
UID: NF:shlobj.INewShortcutHookA.SetFolder
title: INewShortcutHookA::SetFolder (shlobj.h)
description: Sets the folder name for the shortcut object. (ANSI)
helpviewer_keywords: ["INewShortcutHook interface [Windows Shell]","SetFolder method","INewShortcutHook::SetFolder","INewShortcutHookA","INewShortcutHookA.SetFolder","INewShortcutHookA::SetFolder","INewShortcutHookW","INewShortcutHookW::SetFolder","SetFolder","SetFolder method [Windows Shell]","SetFolder method [Windows Shell]","INewShortcutHook interface","_win32_INewShortcutHook_SetFolder","shell.INewShortcutHook_SetFolder","shlobj/INewShortcutHook::SetFolder"]
old-location: shell\INewShortcutHook_SetFolder.htm
tech.root: shell
ms.assetid: 7f402d36-58cf-4912-af21-f8271eee98e4
ms.date: 12/05/2018
ms.keywords: INewShortcutHook interface [Windows Shell],SetFolder method, INewShortcutHook::SetFolder, INewShortcutHookA, INewShortcutHookA.SetFolder, INewShortcutHookA::SetFolder, INewShortcutHookW, INewShortcutHookW::SetFolder, SetFolder, SetFolder method [Windows Shell], SetFolder method [Windows Shell],INewShortcutHook interface, _win32_INewShortcutHook_SetFolder, shell.INewShortcutHook_SetFolder, shlobj/INewShortcutHook::SetFolder
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
 - INewShortcutHookA::SetFolder
 - shlobj/INewShortcutHookA::SetFolder
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
 - INewShortcutHook.SetFolder
 - INewShortcutHookA::SetFolder
 - INewShortcutHookW::SetFolder
---

# INewShortcutHookA::SetFolder


## -description

Sets the folder name for the shortcut object.

## -parameters

### -param pcszFolder

TBD




#### - pszFolder [in]

Type: <b>PCTSTR</b>

A pointer to a string that contains the folder name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

