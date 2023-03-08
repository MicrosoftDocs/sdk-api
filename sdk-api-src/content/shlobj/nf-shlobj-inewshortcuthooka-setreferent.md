---
UID: NF:shlobj.INewShortcutHookA.SetReferent
title: INewShortcutHookA::SetReferent (shlobj.h)
description: Sets the referent of the shortcut object. (ANSI)
helpviewer_keywords: ["INewShortcutHook interface [Windows Shell]","SetReferent method","INewShortcutHook::SetReferent","INewShortcutHookA","INewShortcutHookA interface [Windows Shell]","SetReferent method","INewShortcutHookA.SetReferent","INewShortcutHookA::SetReferent","INewShortcutHookW","INewShortcutHookW interface [Windows Shell]","SetReferent method","INewShortcutHookW::SetReferent","SetReferent","SetReferent method [Windows Shell]","SetReferent method [Windows Shell]","INewShortcutHook interface","SetReferent method [Windows Shell]","INewShortcutHookA interface","SetReferent method [Windows Shell]","INewShortcutHookW interface","_win32_INewShortcutHook_SetReferent","shell.INewShortcutHook_SetReferent","shlobj/INewShortcutHook::SetReferent","shlobj/INewShortcutHookA::SetReferent","shlobj/INewShortcutHookW::SetReferent"]
old-location: shell\INewShortcutHook_SetReferent.htm
tech.root: shell
ms.assetid: 402d305e-1657-45c2-9f0d-04703c8d6e5c
ms.date: 12/05/2018
ms.keywords: INewShortcutHook interface [Windows Shell],SetReferent method, INewShortcutHook::SetReferent, INewShortcutHookA, INewShortcutHookA interface [Windows Shell],SetReferent method, INewShortcutHookA.SetReferent, INewShortcutHookA::SetReferent, INewShortcutHookW, INewShortcutHookW interface [Windows Shell],SetReferent method, INewShortcutHookW::SetReferent, SetReferent, SetReferent method [Windows Shell], SetReferent method [Windows Shell],INewShortcutHook interface, SetReferent method [Windows Shell],INewShortcutHookA interface, SetReferent method [Windows Shell],INewShortcutHookW interface, _win32_INewShortcutHook_SetReferent, shell.INewShortcutHook_SetReferent, shlobj/INewShortcutHook::SetReferent, shlobj/INewShortcutHookA::SetReferent, shlobj/INewShortcutHookW::SetReferent
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
 - INewShortcutHookA::SetReferent
 - shlobj/INewShortcutHookA::SetReferent
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
 - INewShortcutHookA.SetReferent
 - INewShortcutHookW.SetReferent
 - INewShortcutHook.SetReferent
 - INewShortcutHookA::SetReferent
 - INewShortcutHookW::SetReferent
---

# INewShortcutHookA::SetReferent


## -description

Sets the referent of the shortcut object.

## -parameters

### -param pcszReferent

TBD

### -param hwnd

TBD

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window that will be used as the parent if the object needs to display a message box or dialog box. This value can be <b>NULL</b>.


#### - pszReferent [in]

Type: <b>PCTSTR</b>

A pointer to a string that contains the referent.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For Internet shortcut objects, this method is the same as <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)">IUniformResourceLocator::SetURL</a>.
