---
UID: NF:shobjidl_core.ITaskbarList.SetActiveAlt
title: ITaskbarList::SetActiveAlt (shobjidl_core.h)
description: Marks a taskbar item as active but does not visually activate it.
helpviewer_keywords: ["ITaskbarList interface [Windows Shell]","SetActiveAlt method","ITaskbarList.SetActiveAlt","ITaskbarList::SetActiveAlt","SetActiveAlt","SetActiveAlt method [Windows Shell]","SetActiveAlt method [Windows Shell]","ITaskbarList interface","_win32_ITaskbarList_SetActiveAlt","shell.ITaskbarList_SetActiveAlt","shobjidl_core/ITaskbarList::SetActiveAlt"]
old-location: shell\ITaskbarList_SetActiveAlt.htm
tech.root: shell
ms.assetid: b9d08a72-6a4d-483b-bf12-3f78e1d2237a
ms.date: 12/05/2018
ms.keywords: ITaskbarList interface [Windows Shell],SetActiveAlt method, ITaskbarList.SetActiveAlt, ITaskbarList::SetActiveAlt, SetActiveAlt, SetActiveAlt method [Windows Shell], SetActiveAlt method [Windows Shell],ITaskbarList interface, _win32_ITaskbarList_SetActiveAlt, shell.ITaskbarList_SetActiveAlt, shobjidl_core/ITaskbarList::SetActiveAlt
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
 - ITaskbarList::SetActiveAlt
 - shobjidl_core/ITaskbarList::SetActiveAlt
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
 - ITaskbarList.SetActiveAlt
---

# ITaskbarList::SetActiveAlt


## -description

Marks a taskbar item as active but does not visually activate it.

## -parameters

### -param hwnd

Type: <b>HWND</b>

A handle to the window to be marked as active.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SetActiveAlt</b> marks the item associated with <i>hwnd</i> as the currently active item for the window's process without changing the pressed state of any item. Any user action that would activate a different tab in that process will activate the tab associated with <i>hwnd</i> instead. The active state of the window's item is not guaranteed to be preserved when the process associated with <i>hwnd</i> is not active. To ensure that a given tab is always active, call <b>SetActiveAlt</b> whenever any of your windows are activated. Calling <b>SetActiveAlt</b> with a <b>NULL</b> <i>hwnd</i> clears this state.

