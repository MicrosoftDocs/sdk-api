---
UID: NF:shlobj.INewShortcutHookW.GetName
title: INewShortcutHookW::GetName (shlobj.h)
description: Gets the file name of the shortcut object, without the extension.helpviewer_keywords: ["GetName","GetName method [Windows Shell]","GetName method [Windows Shell]","INewShortcutHook interface","INewShortcutHook interface [Windows Shell]","GetName method","INewShortcutHook::GetName","INewShortcutHookA","INewShortcutHookA::GetName","INewShortcutHookW","INewShortcutHookW.GetName","INewShortcutHookW::GetName","_win32_INewShortcutHook_GetName","shell.INewShortcutHook_GetName","shlobj/INewShortcutHook::GetName"]
old-location: shell\INewShortcutHook_GetName.htm
tech.root: shell
ms.assetid: 5eb4a3ce-74ce-4b97-bb5e-67cab82401ec
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],INewShortcutHook interface, INewShortcutHook interface [Windows Shell],GetName method, INewShortcutHook::GetName, INewShortcutHookA, INewShortcutHookA::GetName, INewShortcutHookW, INewShortcutHookW.GetName, INewShortcutHookW::GetName, _win32_INewShortcutHook_GetName, shell.INewShortcutHook_GetName, shlobj/INewShortcutHook::GetName
f1_keywords:
- shlobj/INewShortcutHook.GetName
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
- INewShortcutHook.GetName
- INewShortcutHookA::GetName
- INewShortcutHookW::GetName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INewShortcutHookW::GetName


## -description


Gets the file name of the shortcut object, without the extension.


## -parameters




### -param pszName [out]

Type: <b>PTSTR</b>

A pointer to a string that receives the name.


### -param cchName

Type: <b>int</b>

The size of the buffer at <i>pszName</i>, in characters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



