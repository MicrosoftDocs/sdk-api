---
UID: NF:shlobj.INewShortcutHookW.GetExtension
title: INewShortcutHookW::GetExtension (shlobj.h)

description: Gets the file name extension for the shortcut object.
old-location: shell\INewShortcutHook_GetExtension.htm
tech.root: shell
ms.assetid: ccb54291-7c87-4783-af25-549704371878

ms.date: 12/05/2018
ms.keywords: GetExtension, GetExtension method [Windows Shell], GetExtension method [Windows Shell],INewShortcutHook interface, INewShortcutHook interface [Windows Shell],GetExtension method, INewShortcutHook::GetExtension, INewShortcutHookA, INewShortcutHookA::GetExtension, INewShortcutHookW, INewShortcutHookW.GetExtension, INewShortcutHookW::GetExtension, _win32_INewShortcutHook_GetExtension, shell.INewShortcutHook_GetExtension, shlobj/INewShortcutHook::GetExtension
ms.topic: method
f1_keywords: 
 - "shlobj/INewShortcutHook.GetExtension"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INewShortcutHookW::GetExtension


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



