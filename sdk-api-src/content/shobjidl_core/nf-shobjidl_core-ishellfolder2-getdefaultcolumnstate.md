---
UID: NF:shobjidl_core.IShellFolder2.GetDefaultColumnState
title: IShellFolder2::GetDefaultColumnState (shobjidl_core.h)
description: Gets the default state for a specified column.
helpviewer_keywords: ["GetDefaultColumnState","GetDefaultColumnState method [Windows Shell]","GetDefaultColumnState method [Windows Shell]","IShellFolder2 interface","IShellFolder2 interface [Windows Shell]","GetDefaultColumnState method","IShellFolder2.GetDefaultColumnState","IShellFolder2::GetDefaultColumnState","SHCOLSTATE_EXTENDED","SHCOLSTATE_HIDDEN","SHCOLSTATE_ONBYDEFAULT","SHCOLSTATE_PREFER_VARCMP","SHCOLSTATE_SECONDARYUI","SHCOLSTATE_SLOW","SHCOLSTATE_TYPE_DATE","SHCOLSTATE_TYPE_INT","SHCOLSTATE_TYPE_STR","_win32_IShellFolder2_GetDefaultColumnState","shell.IShellFolder2_GetDefaultColumnState","shobjidl_core/IShellFolder2::GetDefaultColumnState"]
old-location: shell\IShellFolder2_GetDefaultColumnState.htm
tech.root: shell
ms.assetid: 3f55acbf-1e15-42c3-a610-c5742e74883d
ms.date: 12/05/2018
ms.keywords: GetDefaultColumnState, GetDefaultColumnState method [Windows Shell], GetDefaultColumnState method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDefaultColumnState method, IShellFolder2.GetDefaultColumnState, IShellFolder2::GetDefaultColumnState, SHCOLSTATE_EXTENDED, SHCOLSTATE_HIDDEN, SHCOLSTATE_ONBYDEFAULT, SHCOLSTATE_PREFER_VARCMP, SHCOLSTATE_SECONDARYUI, SHCOLSTATE_SLOW, SHCOLSTATE_TYPE_DATE, SHCOLSTATE_TYPE_INT, SHCOLSTATE_TYPE_STR, _win32_IShellFolder2_GetDefaultColumnState, shell.IShellFolder2_GetDefaultColumnState, shobjidl_core/IShellFolder2::GetDefaultColumnState
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder2::GetDefaultColumnState
 - shobjidl_core/IShellFolder2::GetDefaultColumnState
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
 - IShellFolder2.GetDefaultColumnState
---

# IShellFolder2::GetDefaultColumnState


## -description

Gets the default state for a specified column.

## -parameters

### -param iColumn [in]

Type: <b>UINT</b>

An integer that specifies the column number.

### -param pcsFlags [out]

Type: <b>SHCOLSTATEF*</b>

A pointer to a value that contains flags that indicate the default column state. This parameter can include a combination of the following flags.



#### SHCOLSTATE_TYPE_STR

A string.



#### SHCOLSTATE_TYPE_INT

An integer.



#### SHCOLSTATE_TYPE_DATE

A date.



#### SHCOLSTATE_ONBYDEFAULT

Should be shown by default in the Windows Explorer Details view.



#### SHCOLSTATE_SLOW

Recommends that the folder view extract column information asynchronously, on a background thread, because extracting this information can be time consuming.



#### SHCOLSTATE_EXTENDED

Provided by a handler, not the folder object.



#### SHCOLSTATE_SECONDARYUI

Not displayed in the shortcut menu, but listed in the More dialog box.



#### SHCOLSTATE_HIDDEN

Not displayed in the user interface.



#### SHCOLSTATE_PREFER_VARCMP

Uses default sorting rather than <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">CompareIDs</a> to get the sort order.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.