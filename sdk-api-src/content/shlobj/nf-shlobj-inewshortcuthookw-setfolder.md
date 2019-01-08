---
UID: NF:shlobj.INewShortcutHookW.SetFolder
title: INewShortcutHookW::SetFolder
author: windows-sdk-content
description: Sets the folder name for the shortcut object.
old-location: shell\INewShortcutHook_SetFolder.htm
tech.root: shell
ms.assetid: 7f402d36-58cf-4912-af21-f8271eee98e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INewShortcutHook interface [Windows Shell],SetFolder method, INewShortcutHook::SetFolder, INewShortcutHookA, INewShortcutHookA::SetFolder, INewShortcutHookW, INewShortcutHookW.SetFolder, INewShortcutHookW::SetFolder, SetFolder, SetFolder method [Windows Shell], SetFolder method [Windows Shell],INewShortcutHook interface, _win32_INewShortcutHook_SetFolder, shell.INewShortcutHook_SetFolder, shlobj/INewShortcutHook::SetFolder
ms.topic: method
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
 - INewShortcutHook.SetFolder
 - INewShortcutHookA::SetFolder
 - INewShortcutHookW::SetFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INewShortcutHookW::SetFolder


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



