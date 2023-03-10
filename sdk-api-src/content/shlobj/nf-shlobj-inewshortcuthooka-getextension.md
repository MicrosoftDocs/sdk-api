---
UID: NF:shlobj.INewShortcutHookA.GetExtension
title: INewShortcutHookA::GetExtension (shlobj.h)
description: Gets the file name extension for the shortcut object. (ANSI)
helpviewer_keywords: ["GetExtension","GetExtension method [Windows Shell]","GetExtension method [Windows Shell]","INewShortcutHook interface","INewShortcutHook interface [Windows Shell]","GetExtension method","INewShortcutHook::GetExtension","INewShortcutHookA","INewShortcutHookA.GetExtension","INewShortcutHookA::GetExtension","INewShortcutHookW","INewShortcutHookW::GetExtension","_win32_INewShortcutHook_GetExtension","shell.INewShortcutHook_GetExtension","shlobj/INewShortcutHook::GetExtension"]
old-location: shell\INewShortcutHook_GetExtension.htm
tech.root: shell
ms.assetid: ccb54291-7c87-4783-af25-549704371878
ms.date: 12/05/2018
ms.keywords: GetExtension, GetExtension method [Windows Shell], GetExtension method [Windows Shell],INewShortcutHook interface, INewShortcutHook interface [Windows Shell],GetExtension method, INewShortcutHook::GetExtension, INewShortcutHookA, INewShortcutHookA.GetExtension, INewShortcutHookA::GetExtension, INewShortcutHookW, INewShortcutHookW::GetExtension, _win32_INewShortcutHook_GetExtension, shell.INewShortcutHook_GetExtension, shlobj/INewShortcutHook::GetExtension
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
 - INewShortcutHookA::GetExtension
 - shlobj/INewShortcutHookA::GetExtension
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
 - INewShortcutHook.GetExtension
 - INewShortcutHookA::GetExtension
 - INewShortcutHookW::GetExtension
---

# INewShortcutHookA::GetExtension


## -description

Gets the file name extension for the shortcut object.

## -parameters

### -param pszExtension [out]

Type: <b>PTSTR</b>

Pointer to a string that receives the extension.

### -param cchExtension

Type: <b>int</b>

The size of the buffer at <i>pszExtension</i>, in characters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

