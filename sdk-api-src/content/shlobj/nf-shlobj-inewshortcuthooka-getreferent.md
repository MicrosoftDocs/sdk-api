---
UID: NF:shlobj.INewShortcutHookA.GetReferent
title: INewShortcutHookA::GetReferent (shlobj.h)
description: Gets the referent of the shortcut object. (ANSI)
helpviewer_keywords: ["GetReferent","GetReferent method [Windows Shell]","GetReferent method [Windows Shell]","INewShortcutHook interface","INewShortcutHook interface [Windows Shell]","GetReferent method","INewShortcutHook::GetReferent","INewShortcutHookA","INewShortcutHookA.GetReferent","INewShortcutHookA::GetReferent","INewShortcutHookW","INewShortcutHookW::GetReferent","_win32_INewShortcutHook_GetReferent","shell.INewShortcutHook_GetReferent","shlobj/INewShortcutHook::GetReferent"]
old-location: shell\INewShortcutHook_GetReferent.htm
tech.root: shell
ms.assetid: 856f15bb-f9a8-4114-9a18-5abc21bef534
ms.date: 12/05/2018
ms.keywords: GetReferent, GetReferent method [Windows Shell], GetReferent method [Windows Shell],INewShortcutHook interface, INewShortcutHook interface [Windows Shell],GetReferent method, INewShortcutHook::GetReferent, INewShortcutHookA, INewShortcutHookA.GetReferent, INewShortcutHookA::GetReferent, INewShortcutHookW, INewShortcutHookW::GetReferent, _win32_INewShortcutHook_GetReferent, shell.INewShortcutHook_GetReferent, shlobj/INewShortcutHook::GetReferent
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
 - INewShortcutHookA::GetReferent
 - shlobj/INewShortcutHookA::GetReferent
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
 - INewShortcutHook.GetReferent
 - INewShortcutHookA::GetReferent
 - INewShortcutHookW::GetReferent
---

# INewShortcutHookA::GetReferent


## -description

Gets the referent of the shortcut object.

## -parameters

### -param pszReferent

Type: <b>PTSTR</b>

A pointer to a string that receives the referent.

### -param cchReferent

Type: <b>int</b>

The size of the buffer at <i>pszReferent</i>, in characters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For Internet shortcut objects, this method is the same as <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565674(v=vs.85)">IUniformResourceLocator::GetURL</a>.
