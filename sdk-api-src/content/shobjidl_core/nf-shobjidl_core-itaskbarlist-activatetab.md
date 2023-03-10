---
UID: NF:shobjidl_core.ITaskbarList.ActivateTab
title: ITaskbarList::ActivateTab (shobjidl_core.h)
description: Activates an item on the taskbar. The window is not actually activated; the window's item on the taskbar is merely displayed as active.
helpviewer_keywords: ["ActivateTab","ActivateTab method [Windows Shell]","ActivateTab method [Windows Shell]","ITaskbarList interface","ITaskbarList interface [Windows Shell]","ActivateTab method","ITaskbarList.ActivateTab","ITaskbarList::ActivateTab","_win32_ITaskbarList_ActivateTab","shell.ITaskbarList_ActivateTab","shobjidl_core/ITaskbarList::ActivateTab"]
old-location: shell\ITaskbarList_ActivateTab.htm
tech.root: shell
ms.assetid: 1dc95768-62a5-4784-9f4f-96bebdd38c2b
ms.date: 12/05/2018
ms.keywords: ActivateTab, ActivateTab method [Windows Shell], ActivateTab method [Windows Shell],ITaskbarList interface, ITaskbarList interface [Windows Shell],ActivateTab method, ITaskbarList.ActivateTab, ITaskbarList::ActivateTab, _win32_ITaskbarList_ActivateTab, shell.ITaskbarList_ActivateTab, shobjidl_core/ITaskbarList::ActivateTab
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
 - ITaskbarList::ActivateTab
 - shobjidl_core/ITaskbarList::ActivateTab
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
 - ITaskbarList.ActivateTab
---

# ITaskbarList::ActivateTab


## -description

Activates an item on the taskbar. The window is not actually activated; the window's item on the taskbar is merely displayed as active.

## -parameters

### -param hwnd

Type: <b>HWND</b>

A handle to the window on the taskbar to be displayed as active.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

