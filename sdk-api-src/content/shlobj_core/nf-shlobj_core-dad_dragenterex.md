---
UID: NF:shlobj_core.DAD_DragEnterEx
title: DAD_DragEnterEx function (shlobj_core.h)
description: Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. (DAD_DragEnterEx)
helpviewer_keywords: ["DAD_DragEnterEx","DAD_DragEnterEx function [Windows Shell]","shell.DAD_DragEnterEx","shell_DAD_DragEnterEx","shlobj_core/DAD_DragEnterEx"]
old-location: shell\DAD_DragEnterEx.htm
tech.root: shell
ms.assetid: 32f98df7-e357-4d17-9e33-f162a6ffb7ed
ms.date: 12/05/2018
ms.keywords: DAD_DragEnterEx, DAD_DragEnterEx function [Windows Shell], shell.DAD_DragEnterEx, shell_DAD_DragEnterEx, shlobj_core/DAD_DragEnterEx
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_DragEnterEx
 - shlobj_core/DAD_DragEnterEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - DAD_DragEnterEx
---

# DAD_DragEnterEx function


## -description

<p class="CCE_Message">[<b>DAD_DragEnterEx</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragenter">ImageList_DragEnter</a> instead.
      ]

Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window.

## -parameters

### -param hwndTarget

Type: <b>HWND</b>

A handle to the window that owns the drag image.

### -param ptStart

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The coordinates at which to begin displaying the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.
