---
UID: NF:shobjidl_core.IShellFolder2.GetDefaultColumnState
title: IShellFolder2::GetDefaultColumnState
author: windows-sdk-content
description: Gets the default state for a specified column.
old-location: shell\IShellFolder2_GetDefaultColumnState.htm
tech.root: Shell
ms.assetid: 3f55acbf-1e15-42c3-a610-c5742e74883d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetDefaultColumnState, GetDefaultColumnState method [Windows Shell], GetDefaultColumnState method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDefaultColumnState method, IShellFolder2.GetDefaultColumnState, IShellFolder2::GetDefaultColumnState, SHCOLSTATE_EXTENDED, SHCOLSTATE_HIDDEN, SHCOLSTATE_ONBYDEFAULT, SHCOLSTATE_PREFER_VARCMP, SHCOLSTATE_SECONDARYUI, SHCOLSTATE_SLOW, SHCOLSTATE_TYPE_DATE, SHCOLSTATE_TYPE_INT, SHCOLSTATE_TYPE_STR, _win32_IShellFolder2_GetDefaultColumnState, shell.IShellFolder2_GetDefaultColumnState, shobjidl_core/IShellFolder2::GetDefaultColumnState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder2.GetDefaultColumnState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Uses default sorting rather than <a href="https://msdn.microsoft.com/54d805cc-5396-4892-9347-cafc2d90779f">CompareIDs</a> to get the sort order.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



