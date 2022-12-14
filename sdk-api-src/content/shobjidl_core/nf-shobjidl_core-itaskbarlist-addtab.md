---
UID: NF:shobjidl_core.ITaskbarList.AddTab
title: ITaskbarList::AddTab (shobjidl_core.h)
description: Adds an item to the taskbar.
helpviewer_keywords: ["AddTab","AddTab method [Windows Shell]","AddTab method [Windows Shell]","ITaskbarList interface","ITaskbarList interface [Windows Shell]","AddTab method","ITaskbarList.AddTab","ITaskbarList::AddTab","_win32_ITaskbarList_AddTab","shell.ITaskbarList_AddTab","shobjidl_core/ITaskbarList::AddTab"]
old-location: shell\ITaskbarList_AddTab.htm
tech.root: shell
ms.assetid: 47d52ab8-f182-4bfb-8745-ad2d23197088
ms.date: 12/05/2018
ms.keywords: AddTab, AddTab method [Windows Shell], AddTab method [Windows Shell],ITaskbarList interface, ITaskbarList interface [Windows Shell],AddTab method, ITaskbarList.AddTab, ITaskbarList::AddTab, _win32_ITaskbarList_AddTab, shell.ITaskbarList_AddTab, shobjidl_core/ITaskbarList::AddTab
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList::AddTab
 - shobjidl_core/ITaskbarList::AddTab
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
 - ITaskbarList.AddTab
---

# ITaskbarList::AddTab


## -description

Adds an item to the taskbar.

## -parameters

### -param hwnd

Type: <b>HWND</b>

A handle to the window to be added to the taskbar.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any type of window can be added to the taskbar, but it is recommended that the window at least have the <a href="/windows/desktop/winmsg/window-styles">WS_CAPTION</a> style.

Any window added with this method must be removed with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-deletetab">DeleteTab</a> method when the added window is destroyed.